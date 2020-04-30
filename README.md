# mysql57-ja
MySQL5.7の公式のDockerイメージに日本語化設定を追加したもの

# 使い方

## Docker Hubからイメージをpull
docker pull kamatimaru/mysql57-ja

## イメージをローカルでビルド
```shell
docker build -t kamatimaru/mysql57-ja .
```

## コンテナ起動
```shell
docker run --name mysql57-ja -e MYSQL_ROOT_PASSWORD=password -d kamatimaru/mysql57-ja:latest
```

## ログイン
```shell
docker exec -it mysql57-ja /bin/bash
```