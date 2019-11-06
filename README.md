Docker container of PHP 5.2 with Apache
=======================================

* CentOS 5
* Apache 2 
* PHP 5.2 
* PHP GD 
* PHP PDO 
    * MySQL (`mysql-devel`)
    * PostgreSQL (`postgresql-devel`)
    * Oracle 11g (Oracle Instant Client 11.2)
    * SQLite (`sqlite-devel`)

```
docker build -t php-5.2-apache ./
```


```
docker run \
    -d \
    -p 49160:80 \
    -v ${HOME}:/data \
    -v ${PROJ_DIR}/htdocs:/var/www/html \
    php-5.2-apache
```

Jean Sauzem <jsauzem@gmail.com> <jean.marques@meta.com.br>
