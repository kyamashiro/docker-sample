# docker build -t greet .
# winpty docker container run -it --rm greet asa

# Build Image
FROM golang:1.8.4-jessie AS builder

# Install dependencies
WORKDIR /go/src/github.com/asashiho/greet
RUN go get -d -v github.com/urfave/cli

# Build modules
# ローカルのmain.goをコンテナにコピー
# Go buildコマンドでビルドし、greetというバイナリファイルを作成する
COPY main.go .
RUN GOOS=linux go build -a -o greet .

# Production Image
# プロダクション環境用のベースイメージ
FROM busybox
WORKDIR /opt/greet/bin

# Deploy modules
# builderという名前のimageからコピーする
COPY --from=builder /go/src/github.com/asashiho/greet/ .
ENTRYPOINT ["./greet"]