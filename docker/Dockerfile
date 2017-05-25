from registry.cn-hangzhou.aliyuncs.com/hc/jdk8
MAINTAINER xiaoyu
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ADD java-quotation-fetcher-1.0-SNAPSHOT.jar java-quotation-fetcher-1.0-SNAPSHOT.jar
ADD jtds-1.2.4.jar jtds-1.2.4.jar
ADD slf4j-api-1.7.2.jar slf4j-api-1.7.2.jar
ADD gson-2.3.1.jar gson-2.3.1.jar
ADD log4j-1.2.17.jar log4j-1.2.17.jar
ADD slf4j-log4j12-1.7.2.jar slf4j-log4j12-1.7.2.jar
WORKDIR /application
#RUN "java -cp /application/java-quotation-fetcher-1.0-SNAPSHOT.jar:/application/gson-2.3.1.jar:/application/jtds-1.2.4.jar:/application/log4j-1.2.17.jar:/application/slf4j-api-1.7.2.jar:/application/slf4j-log4j12-1.7.2.jar com.ytx.quotation.Fetcher"
ENTRYPOINT ["java","-cp","./java-quotation-fetcher-1.0-SNAPSHOT.jar:./gson-2.3.1.jar:./jtds-1.2.4.jar:./log4j-1.2.17.jar:./slf4j-api-1.7.2.jar:./slf4j-log4j12-1.7.2.jar","com.ytx.quotation.Fetcher"]
