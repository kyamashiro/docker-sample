#Ubuntuベースイメージ
FROM ubuntu:latest

#Nginxのインストール
RUN apt-get update && apt-get install -y -q nginx

#ファイルのコピー
COPY index.html /usr/share/nginx/html/

#Nginxの起動
CMD ["nginx", "-g". "daemon off;"]