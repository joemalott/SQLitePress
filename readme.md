# SQLitepress


SQLitepress is the answer to the question “How quickly can I get a local instance of WordPress up and running?”

The answer, about one minute.
Clone the repository:

`git clone http://github.com/joemalott/sqlitepress your-project-name`

Then simply move into your project directory

`cd your-project-name`

Then fire up PHP server. On OSX this is

`php -S localhost:8000`

Open a browser at http://localhost:8000 and after inputting admin credentials you are immediately in a new instance of WordPress. With the power of SQLite you now have a highly portable instance to begin tinkering with.

It is NOT recommended for production environments. More for curious developers to begin tinkering with and later migrate over the theme/plugin to a normal instance of WordPress.

Happy theme/plugin development.
