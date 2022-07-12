FROM maven:3.3-jdk-8 AS builder

RUN mkdir /javaapp

WORKDIR /javaapp

COPY . .

RUN mvn install

FROM tomcat:8.0-alpine

COPY --from=builder /javaapp/target/*.war /usr/local/tomcat/webapps
