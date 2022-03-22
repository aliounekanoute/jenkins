FROM maven:3.8.4-jdk-11
RUN mkdir /project
COPY . /project

WORKDIR /project

RUN mvn package

ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom", "-Dblabla", "-jar","/project/target/jenkins-app-1.0-SNAPSHOT.jar"]
