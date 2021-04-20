FROM openjdk:8

ARG PROFILE
ARG ADDITIONAL_OPTS 

ENV PROFILE=${PROFILE}
ENV ADDITIONAL=${ADDITIONAL_OPTS}

WORKDIR /opt/spring_boot

COPY /target/spring-boot*.jar spring_boot_docker.jar

SHELL [ "/bin/sh", "-c" ]

EXPOSE 5005
EXPOSE 8080


CMD java ${ADDITIONAL_OPTS} -jar spring_boot_docker.jar --spring.profiles.active=${PROFILE}

