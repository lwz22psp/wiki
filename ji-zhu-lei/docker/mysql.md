# MySql

```bash
sudo docker run --name mysql -d --rm \
-v [config path]:/etc/mysql/conf.d \
-v [data path]:/var/lib/mysql \
-p [port]:3306 -e MYSQL_ROOT_PASSWORD=[root pwd] mysql:5.7.22
```



