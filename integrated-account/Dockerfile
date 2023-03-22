FROM openjdk:8-jdk-alpine as builder

LABEL author="yuluo" \
	email="yuluo829@aliyun.com"

ADD ./integrated-account/target/integrated-account-*.jar /app.jar

RUN sh -c 'touch /app.jar'  #修改这个文件的访问时间和修改时间为当前时间
EXPOSE 8012

ENTRYPOINT ["java", "-jar","/app.jar"]