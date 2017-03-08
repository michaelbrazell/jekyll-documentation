---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
# layout: home
layout: page
---
## Table of Contents
* Server Overview
  * Front-end Links
  * How to Connect
* Configuration and Installation Information
  * Apache & WordPress
  * MariaDB (MySQL)
  * PhpMyAdmin configuration
* Contact

* * *

## Server Overview
The Web Standards server runs on a headless CentOS7 server located in Natick.
The environment is a standard Linux install and was initially setup by the Linux install team contacted by SSG.
While SSG setup the initial environment, they only support the environment in case of a hardware outage
or some other technical issue.  Otherwise, the server is maintained by Front-end developers in ePS.

The Web Standards site is running in the following environment:
* CentOS7.2 VM
* PHP 5.1.x
* MariaDB 5.4.x _(MariaDB is an open source MySQL project)_
* Apache 2.2.x
* PHPMyAdmin 2.x
* WordPress 4.7.2 _(At time of install)_

### Front-end Links
* [http://web-standards.mathworks.com](Web Standards Home)
* [http://web-standards.mathworks.com/wp-admin](Web Standards Admin Dashboard)
* [http://web-standards/phpmyadmin](PHPMyAdmin GUI) _(Note: Only accessible to specific IPs, CTRL+F for PHPMyAdmin Config)_

* * *

## How to Connect
Connect to the server using SSH.  In your terminal, console, or other command line tool, enter:

`$ ssh web-standards`

or

`$ ssh 172.31.49.97`

_(Note: the `$` designates a console command but your environment may differ)_

This will connect you to the server and you will be prompted for your account password.

> Important: You can only connect and access the server if your MW Unix account has permissions.
Contact SSG on the virtualization team to request access.  _As of March 2017, only Mike Murray and Ryan Johnson
have access._

After connecting, you will be in your unix home directory.

* * *

## Configuration and Installation Information
### Apache & WordPress
Apache is installed in `/var/html/` and the WordPress instance is installed at `/var/html/www/`

To navigate to the WP directory:

`$ cd /var/html/www`

Apache's configuration is located:

`$ TO DO: Add Apache configuration location`

### MariaDB (MySQL)
The server uses MariaDB as the database, and the database is stored locally on the box (`localhost`).

**MariaDB Information for WordPress**
* **Host**: localhost
* **Username**: Root
* **Password**: (Too Add)
* **Database**: webstandardsdb

### PhpMyAdmin configuration
For security reasons, PhpMyAdmin is locked only to specific IPs within MW.  To add a new IP to the configuration:

`$ cd /etc/httpd/conf.d
$ vi phpMyAdmin.conf`

Use Vim to edit the configuration and add the IP of the machine you want to use to connect to the PhpMyAdmin UI.
If you are new to Vim, Google a user guide, but the typical commands you'll use are:

* When first opening the file, press the `I` key, this puts you into `INSERT` mode.
* Make your changes as needed while in `INSERT` mode
* When finished making changes, hit the `ESC` key, which allows you to type the next command:
* Type `:wq` and hit enter.  This will `WRITE` your changes to the file and then `QUIT` vim back to the file system.
* If you've made a mistake, you can open the command prompt in vim (`ESC` key) and type `q!` which will quit without saving

* * *

## Contact
### Mike Murray
* [MathWorks email](mailto:mike.murray@mathworks.com)
* [Personal email](mailto:michaelbrazell@gmail.com)
* Extension: x7067 (TODO add number)
