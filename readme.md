# SQLitePress (archived)

**This project is retired. Use [WordPress Playground](https://developer.wordpress.org/playground/) instead.**

```
npx @wp-playground/cli@latest start
```

That gives you a local WordPress on SQLite in seconds. No Docker, no MySQL, no vendored copy of WordPress core, and nothing to keep updated.

## Why this is archived

SQLitePress was built in 2017 to answer one question: how fast can you get a local WordPress running? The trick was to vendor a full WordPress checkout into git alongside the SQLite drop-in, so `git clone` plus `php -S localhost:8000` was all you needed.

It worked, but every WordPress release meant re-vendoring the entire core tree by hand. I did that five times in nine years and the repo was usually out of date. The last snapshot here is WordPress 6.9 with the official [sqlite-database-integration](https://github.com/WordPress/sqlite-database-integration) plugin.

The tooling caught up. WordPress Playground runs PHP compiled to WebAssembly against SQLite, so there is no core to vendor and no version to chase.

## What to use now

Playground CLI, for a throwaway or persistent local site:

```
npx @wp-playground/cli@latest start
```

The site persists between runs under `~/.wordpress-playground/sites/`. Useful flags:

- `--wp=6.9` and `--php=8.3` to pin versions
- `--mount=/host/path:/vfs/path` to develop a theme or plugin in place
- `--auto-mount` to detect and mount the current project
- `--port=9400` to change the port
- `--reset` to wipe the stored site and start clean

If you would rather have a GUI, [Studio](https://developer.wordpress.com/studio/) is a free desktop app built on the same WebAssembly and SQLite engine, with one-click sites on macOS, Windows and Linux.

If you want SQLite on a normal WordPress install rather than a Playground one, install the [sqlite-database-integration](https://github.com/WordPress/sqlite-database-integration) plugin directly. It is still a feature plugin and has not been merged into core. Its 2025 driver rewrite closed most of the remaining MySQL compatibility gaps.

Neither this project nor SQLite-backed WordPress in general is meant for production.

## The old instructions

Kept for anyone who lands here from an old link. This repository still works as it did.

```
git clone https://github.com/joemalott/SQLitePress your-project-name
cd your-project-name
php -S localhost:8000
```

Open http://localhost:8000, enter admin credentials, and you have WordPress 6.9 on SQLite. You will want to update WordPress once you are in.
