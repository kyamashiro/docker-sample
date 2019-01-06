# docker build -t sample .
# docker container run -it sample
# CMD命令は実行時に上書きできる
# docker container run -it sample -d 2
FROM ubuntu:16.04

ENTRYPOINT ["top"]
CMD ["-d", "10"]