# graphviz
graphvizをubuntuにインストールするための環境

## 起動方法



#### 1. 下記コマンドでビルドとコンテナ起動を行う
```
$ docker-compose up -d app
```

#### 2. コンテナにアクセスし、ライブラリをインストール
```
$ docker-compose exec  app /bin/bash

root@aa1519d1a400:/workspace# pip install --upgrade pip
root@aa1519d1a400:/workspace# pip install -U -r requirements.txt
root@aa1519d1a400:/workspace# pip freeze > requirements.txt
```

#### 3. jupyter を起動
```
root@aa1519d1a400:/workspace# jupyter lab --allow-root --no-browser --NotebookApp.token='' --port 8888 --ip=0.0.0.0
```
#### 4.http://localhost:8080/ にアクセス
