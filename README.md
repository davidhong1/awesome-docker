# run mysql
```shell
# mkdir -p ~/docker/data/var/lib/mysql
docker-compose -f ARM-MySQL57-docker-compose.yml up -d
docker exec -it awesome-docker-mysql57-1 mysql -uroot -p

# 创建其他用户
CREATE USER 'your_username_here'@'%' IDENTIFIED BY 'your_password_here';
# 授予用户所有权限并允许所有主机访问
GRANT ALL PRIVILEGES ON *.* TO 'your_username_here'@'%' WITH GRANT OPTION;
# 刷新权限
FLUSH PRIVILEGES;
```

# remove mysql
```shell
docker-compose -f ARM-MySQL57-docker-compose.yml down
# rm -rf ~/docker/data/var/lib/mysql
```

# run redis
```shell
# mkdir -p ~/docker/data/var/lib/mysql
docker-compose -f Redis-docker-compose.yml up -d
```

# remove redis
```shell
docker-compose -f Redis-docker-compose.yml down
```

# run MongoDB
```shell
# mkdir -p ~/docker/data/var/lib/mysql
docker-compose -f MongoDB-docker-compose.yml up -d
```

# remove MongoDB
```shell
docker-compose -f MongoDB-docker-compose.yml down
```
