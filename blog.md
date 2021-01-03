## install

- google docker
- set mirror:[http://guide.daocloud.io/dcs/daocloud-9153151.html#Docker加速器-DockerforMac](http://guide.daocloud.io/dcs/daocloud-9153151.html#Docker%E5%8A%A0%E9%80%9F%E5%99%A8-DockerforMac)

## commands

some-mysql is your container name 

```docker
docker ps //check container status
docker kill some-mysql
docker container start some-mysql
docker rm some-mysql
```

## MySql

```bash
docker run --name mysql_test -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 -d mysql:5.7.28
```

- mysql_test:container name
- -e:environment
- 123456:your password
- -p 3306:3306:set your port local-port:container-port

### Container shell access and viewing MySQL logs

The following command line will give you a bash shell inside your mysql container:

```docker
docker exec -it some-mysql bash
```

The log is available through Docker's container log:

```bash
docker logs some-mysql
```

get into mysql 

```docker
mysql -u root -p

show databases;
use some-table;
show tables;
```
