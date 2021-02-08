# mysql57-ja
MySQL5.7の公式のDockerイメージに日本語化設定を追加したもの

# 使い方

## Docker Hubからイメージをpull
```shell
$ docker pull kamatimaru/mysql57-ja
```

## イメージをローカルでビルド
```shell
$ git clone https://github.com/delhi09/docker-mysql57-ja.git
$ cd docker-mysql57-ja
$ docker build -t kamatimaru/mysql57-ja .
```

## コンテナ起動
```shell
$ docker run --name mysql57-ja -e MYSQL_ROOT_PASSWORD=password -d -p 3306:3306 kamatimaru/mysql57-ja:latest
```

## コンテナへのログイン
```shell
$ docker exec -it mysql57-ja /bin/bash
```

## mysqlへのログイン
```shell
$ mysql -u root -p -h 127.0.0.1
Enter password: # 「password」と入力
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 2
Server version: 5.7.30 MySQL Community Server (GPL)

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```