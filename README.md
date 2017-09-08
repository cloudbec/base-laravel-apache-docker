# Laravel Base Image 

This image is a base image for Laravel application served by Apache with mod_php running **php 7**. Must be used as  a first step 

## Stack

- Apache 2 with PHP mod
- PHP 7
- Node 6.6.2 *(Used only to run frontend tasks. Removed from the final image)*


See `How to use this image` section for more details.

![logo PHP](php-logo.png) ![logo Laravel](laravel-logo.png) ![Apache](httpd-logo.png)

[PHP][1]
[Laravel][2]
[Apache][3]

# thanks

thanks to brunogasparin/laravel-apache:5-onbuild for the good work



# Supported tags and respective `Dockerfile` links

# How to use this image


### How to configure PHP for development

This image comes with php-fpm configured to be used in production environment, containing settings which hold 
security, performance and best practices. To customize the php behavior for development environment, `COPY`
 a custom `php.ini` configuration into `/usr/local/etc/php` (you can use the `$PHP_INI_DIR` environment variable) 
 by adding one more line to the Dockerfile above and running the same commands to build and run:

```dockerfile
FROM brunogasparin/laravel-apache:5-onbuild
COPY config/php.ini $PHP_INI_DIR
```

Where `config/` contains your `php.ini` file.

# Useful Links

- [PHP Oficial Image Repository][3]

[1]: http://http://php.net/
[2]: https://laravel.com
[3]: http://httpd.apache.org
