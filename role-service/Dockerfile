from bryandollery/maven-repo as build

WORKDIR /usr/src/app

arg rebuild

run https://github.com/saloyiana/jenkins-k8s.git && \
    cd jenkins-k8s/role-service/
  && \
    mvn clean package

from adoptopenjdk/openjdk11:alpine

copy --from=build "/usr/src/app/jenkins-k8s/role-service/target/role-service-1.0.0.jar" /

cmd ["java", "-jar", "role-service-1.0.0.jar"]

expose 80
