FROM openjdk:10-slim
VOLUME /tmp
ARG JAR_FILE
ARG CONFIG_URI
ARG EUREKA_URI
ENV CONFIG_URI_ENV = ${CONFIG_URI}
ENV EUREKA_URI_ENV = ${EUREKA_URI}
COPY ${JAR_FILE} app.jar
ENTRYPOINT java -Djava.security.egd=file:/dev/./urandom -DCONFIG_URI=${CONFIG_URI_ENV} -DEUREKA_URI=${EUREKA_URI_ENV} -jar /app.jar
