# docker build -t run-sample .
FROM ubuntu:latest

# docker history run-sample
# Shell形式で記述したRUN命令は/bin/sh、EXEC形式で記述したRUN命令はシェルを介さずに実行する
RUN echo Shell形式
RUN ["echo", "EXEC形式"]
RUN ["/bin/bash", "-c", "echo 'EXEC形式でbashを使う'"]