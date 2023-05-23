To work with a full SQL database locally I setup [Caddy](https://caddyserver.com/) with [php-fpm](https://archlinux.org/packages/extra/x86_64/php-fpm/), [phpmyadmin](https://archlinux.org/packages/extra/any/phpmyadmin/) and [MariaDB](https://mariadb.org/).

# Potential Pitfalls

## Caddy & php-fpm are running as different users
They need to at least share a group - for example my web host gives them both www-data roles which controls the php-fpm unix socket at 