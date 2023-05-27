---
dg-publish: true
---
# Setting up CLMP (Caddy, Linux, MariaDB and PHP) Locally for development on Arch
To work with a full SQL database locally I setup [Caddy](https://caddyserver.com/) with [php-fpm](https://archlinux.org/packages/extra/x86_64/php-fpm/), [phpmyadmin](https://archlinux.org/packages/extra/any/phpmyadmin/) and [MariaDB](https://mariadb.org/).

# Potential Pitfalls

## Caddy & php-fpm are running as different users
They need to at least share a group - for example my web host gives them both www-data roles which controls the php-fpm unix socket at `/run/php-fpm/php-fpm.sock`. When they had different users/groups caddy kept complaining with the following message
`dialing backend: dial unix /run/php-fpm/php-fpm.sock: connect: permission denied`

## The website root directory / files aren't permissioned correctly
The files in the website root directory must be owned by a group that is accessible to caddy and php-fpm so they can both serve files from it (caddy handles most types and PHP handles php files)

## PHPMyAdmin - Temp Directory Inaccessible
Go into the phpMyAdmin directory (`/usr/share/webapps/phpMyAdmin/` if you installed it using pacman on arch linux) and create the `tmp` folder and set it to be accessible/owned by the web server group. Edit the `config.inc.php` to include this line:
```php
$cfg['TempDir'] = '/tmp';
```
If it is still not happy, then restart php-fpm and caddy.

## Enabling mysqli
On arch linux, the mysqli plugin (and a bunch more) come preinstalled with the base image, simply edit the `/etc/php/php.ini` file to uncomment the line 
```php
extension=mysqli
```
(line 931 as I write this)

## Caddy Config
```caddyfile
http:// {
	root * /usr/share/webapps/phpMyAdmin/
	
	php_fastcgi unix//run/php-fpm/php-fpm.sock

	file_server
}
```

#Linux #Web