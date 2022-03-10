#### 常用镜像
##### mongodb
```
docker run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=hhb -e MONGO_INITDB_ROOT_PASSWORD=nx123456!  -e MONGO_INITDB_DATABASE=mongo-test mongo:latest

```
##### redis
``` bash
docker run  -d -p 6379:6379 -v /usr/redis/conf:/usr/local/etc/redis --name myredis redis redis-server /usr/local/etc/redis/redis.conf
```

```
#redis配置

bind 0.0.0.0

#设置密码
requirepass foobared

```

##### mysql
```
docker run -dp 3306:3306 -e MYSQL_ROOT_PASSWORD=nx123456! \
-e MYSQL_DATABASE=hhb \
-e MYSQL_USER=hhb \
-e MYSQL_PASSWORD=nx123456! \
--name my-test-mysql \
mysql:5.7.35
```

