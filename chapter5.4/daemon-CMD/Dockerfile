# docker build -t cmd-sample
# docker container run -p 80:80 -d cmd-sample

FROM ubuntu:16.04

RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install nginx

# ポート指定
EXPOSE 80

# サーバの実行 EXEC形式
CMD ["nginx", "-g", "daemon off;"]