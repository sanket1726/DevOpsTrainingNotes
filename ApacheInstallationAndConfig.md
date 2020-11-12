# < `/etc/init.d/apache2` >
### Apache Installation
>Apache is available within Ubuntu’s default software repositories, so we will install it using conventional package management tools.

## Step 1: Install Apache
> `sudo apt-get update`

> `sudo apt-get install apache2`

## Step 2: Adjust the Firewall
>Before we can test Apache, we need to modify our firewall to allow outside access to the default web ports. Assuming that you followed the instructions in the prerequisites, you should have a UFW firewall configured to restrict access to your server.
During installation, Apache registers itself with UFW to provide a few application profiles. We can use these profiles to simplify the process of enabling or disabling access to Apache through our firewall.

> `sudo ufw app list`

> `sudo ufw allow 'Apache Full'`

> `sudo ufw status`

## Step 2: Check your Web Server
> `sudo systemctl status apache2`

> `sudo systemctl start apache2`

> `sudo systemctl stop apache2`

> `sudo systemctl reload apache2`

# TO run make apache2 available in init.d
    `sudo update-rc.d apache2 defaults`

## By default, Apache is configured to start automatically when the server boots. If this is not what you want, you can disable this behavior by typing:

>`sudo systemctl disable apache2`

To re-enable the service to start up at boot, you can type:

`sudo systemctl enable apache2`

Apache should now start automatically when the server boots again.

## Step 5: Get Familiar with Important Apache Files and Directories
* ## Content
> /var/www/html: The actual web content, which by default only consists of the default Apache page you saw earlier, is served out of the /var/www/html directory. This can be changed by altering Apache configuration files.

* ## Server Configuration
> /etc/apache2: The Apache configuration directory. All of the Apache configuration files reside here.

>   /etc/apache2/apache2.conf: The main Apache configuration file. This can be modified to make changes to the Apache global configuration. This file is responsible for loading many of the other files in the configuration directory.

>/etc/apache2/ports.conf: This file specifies the ports that Apache will listen on. By default, Apache listens on port 80 and additionally listens on port 443 when a module providing SSL capabilities is enabled.

>/etc/apache2/sites-available/: The directory where per-site “Virtual Hosts” can be stored. Apache will not use the configuration files found in this directory unless they are linked to the sites-enabled directory (see below). Typically, all server block configuration is done in this directory, and then enabled by linking to the other directory with the a2ensite command.

>/etc/apache2/sites-enabled/: The directory where enabled per-site “Virtual Hosts” are stored. Typically, these are created by linking to configuration files found in the sites-available directory with the a2ensite. Apache reads the configuration files and links found in this directory when it starts or reloads to compile a complete configuration.

>/etc/apache2/conf-available/, /etc/apache2/conf-enabled/: These directories have the same relationship as the sites-available and sites-enabled directories, but are used to store configuration fragments that do not belong in a Virtual Host. Files in the conf-available directory can be enabled with the a2enconf command and disabled with the a2disconf command.

>/etc/apache2/mods-available/, /etc/apache2/mods-enabled/: These directories contain the available and enabled modules, respectively. Files in ending in .load contain fragments to load specific modules, while files ending in .conf contain the configuration for those modules. Modules can be enabled and disabled using the a2enmod and a2dismod command.

* ## Server Logs

>/var/log/apache2/access.log: By default, every request to your web server is recorded in this log file unless Apache is configured to do otherwise.

>/var/log/apache2/error.log: By default, all errors are recorded in this file. The LogLevel directive in the Apache configuration specifies how much detail the error logs will contain.



Fw+NxiKQs7y3J6zTxE8FHk0TwDPuQ8YT1OFhExz2Cws