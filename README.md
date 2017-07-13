
```sh
ghost:Docker-Linux-ApacheNginx-PHP-FPM-MySQL kumbasar$ docker-compose up -d
Starting dockerlinuxapachenginxphpfpmmysql_php_1 ...
Starting dockerlinuxapachenginxphpfpmmysql_php_1
Starting mysql ...
Starting dockerlinuxapachenginxphpfpmmysql_php_1 ... done
Starting dockerlinuxapachenginxphpfpmmysql_web_1 ...
Starting dockerlinuxapachenginxphpfpmmysql_web_1 ... done
ghost:Docker-Linux-ApacheNginx-PHP-FPM-MySQL kumbasar$ docker-compose exec mysqldb bash
root@30b67eb3af95:/# mysql -u root -p
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 3
Server version: 5.7.18 MySQL Community Server (GPL)

Copyright (c) 2000, 2017, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> exit
Bye
root@30b67eb3af95:/# exit
exit
ghost:Docker-Linux-ApacheNginx-PHP-FPM-MySQL kumbasar$ docker-compose ps
                 Name                                Command              State           Ports
--------------------------------------------------------------------------------------------------------
dockerlinuxapachenginxphpfpmmysql_php_1   docker-php-entrypoint php-fpm   Up      9000/tcp
dockerlinuxapachenginxphpfpmmysql_web_1   nginx -g daemon off;            Up      0.0.0.0:80->80/tcp
mysql                                     docker-entrypoint.sh mysqld     Up      0.0.0.0:3306->3306/tcp
ghost:Docker-Linux-ApacheNginx-PHP-FPM-MySQL kumbasar$
```
