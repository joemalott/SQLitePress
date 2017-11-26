## Introduction

The goal of this was to provide a stupidly fast way to implement WordPress locally without the need for MySQL. The goal is to allow theme development to be quick and painless. This should not be used for serious development unless you are looking to utilize SQLite in your own WordPress installations. There are valid arguments for and against this, and use-cases which would factor in a decision of SQLite over MySQL, but the portability and quick setup is a great advantage especially for low-traffic and simple WordPress installations.

## Installation


#### The Simplest Method

The quickest method is to simply clone this repo into any folder using:

~~~~
git clone https://github.com/Coasternerd/Wordpress-SQLite.git .
~~~~

For Mac users, PHP comes pre-installed making this even more convenient. (For Windows users you must first install PHP here: [PHP for Windows](https://www.sitepoint.com/how-to-install-php-on-windows/ "Windows PHP | SitePoint"))

Simply start a server using:

~~~~
php -S localhost:8888
~~~~

Then you can simply visit http://localhost:8888 and see your live site. Note you can use any server port you desire, localhost:8888 is simply a common port for local development.

For WordPress installation, simply Follow WordPress' famous 5-Minute installation and you are in business. Happy Theming/Developing/Testing :-)

#### For a live web server:

For a live web server running PHP version 5.2.4 or greater, you can simply clone this repository into the root of the server or specific app you wish to run WordPress.


#### MAMP or XAMPP:

If you are using MAMP or XAMPP the process is the same. Clone the repo into the web root folder (Typically this is in ~/xampp/htdoc or ~/Mamp/htdocs).  


## Additional Info 

Additional instructions and resources on using the SQLite Integration plugin can be found here:

https://wordpress.org/plugins/sqlite-integration/#installation
