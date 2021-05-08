and-bar
# Docker環境

## Dockerコマンド

### Dockerイメージビルド
```
$ docker image build -t nginx_sample .
-- docker build <オプション> <イメージ名>:<タグ名> <Dockerfileが配置されているディレクトリ>
```

### Dockerコンテナの実行
```
$ docker container run nginx_sample_1
```

#### コンテナの実行を持続したい時
```
$ docker container run -itd nginx_sample_1
```

### Dockerコンテナの停止
```
$ docker container stop nginx_sample_1
```

### Dockerコンテナ内に入る
```
$ docker container exec -it nginx_sample_1 bash
```

## docker-composeコマンド
### 起動
```bash
$ docker-compose up -d

### ビルド有り
$ docker-compose up -d --build
```

### 停止
```bash
$ docker-compose stop
```

### 停止&イメージを削除
```bash
$ docker-compose down --rmi all
```

### コンテナ内に入る
```bash
$ docker-compose exec nginx_sample_1 /bin/bash
```

# nginxの操作
## nginxの起動
```
$ nginx
```

## nginxの停止
```
$ nginx -s stop
```

## ブラウザからアクセス
http://localhost:8085


## 参考資料
  - docker+nginx(ubuntu)でWEBサーバを構築してみる
    - https://blowup-bbs.com/nginx-ubuntu-docker-webserver/
  - 【Nginx】portが占領されてサーバーが起動できないときの対処法
    - https://qiita.com/ngron/items/55a84ef6abce903c4424
