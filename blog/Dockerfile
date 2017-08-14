FROM ubuntu:16.04

#更新软件源，必须要执行，否则可能会出错。
RUN apt-get -y update

RUN apt-get install -y python-dev python-pip
RUN apt-get install -y python-setuptools
RUN apt-get install -y libmysqlclient-dev


RUN mkdir /blog

#设置工作目录
WORKDIR /blog

#将当前目录加入到工作目录中
ADD . /blog


#install any needed pacakges in requirements.txt
RUN pip install -r requirements.txt


#对外暴露端口
EXPOSE 80 8080 8000 5000



#设置环境变量
ENV SPIDER=/blog

















