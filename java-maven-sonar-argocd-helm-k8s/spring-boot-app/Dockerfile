# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM adoptopenjdk/openjdk11:alpine-jre

# Set the JAVA_OPTS environment variable
ENV JAVA_OPTS -Dorg.jenkinsci.plugins.durabletask.BourneShellScript.LAUNCH_DIAGNOSTICS=true

# Simply the artifact path
ARG artifact=/home/mediquity/eclipse-workspace/Jenkins-Zero-To-HeroTarun/java-maven-sonar-argocd-helm-k8s/spring-boot-app/target/spring-boot-web.jar

WORKDIR /opt/google/app

COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["java","-jar","app.jar"]
