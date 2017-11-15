FROM ubuntu:17.10
MAINTAINER ifnoelse "ifnoelse@qq.com"
RUN apt-get update && apt-get install -y apt-utils && apt-get install -y nginx
ADD test.txt /mydate
CMD nginx -g "daemon off;"
EXPOSE 80