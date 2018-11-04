# Description (説明)

This repository is a small template for easily trying flask with docker-compose.  
このリポジトリはdocker-composeでflaskを手軽に試す為の小さなテンプレートです。  

# Preparation (準備)

Please install the following before using this repository.  
このリポジトリを使う前に下記をインストールしておいてください。  

- docker
- docker-compose

# How to use (使い方)

Execute app/main.py at startup. Please change as necessary.  
起動時に app/main.py を実行します。必要に応じて変更してください。  

- startup (起動)

```sh
$ docker-compose up -d
```

- teardown (終了)

```sh
$ docker-compose down
```

- Example of access from client side (クライアント側からのアクセス例)

get

```sh
$ curl http://localhost:5001/
route get. Hello!
```

post

```sh
$ curl http://localhost:5001/reply -X POST -H "Content-Type: application/json" -d '{"keyword": "hoge"}'
{
  "Answer": {
    "Text": "route post. keyword is hoge!"
  },
  "Content-Type": "application/json"
}
```
