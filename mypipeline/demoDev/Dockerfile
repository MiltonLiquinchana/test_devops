FROM debian
USER root
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y tar curl
RUN curl -L https://download.java.net/java/GA/jdk21/fd2272bbf8e04c3dbaee13770090416c/35/GPL/openjdk-21_linux-x64_bin.tar.gz | tar xvz -C /opt/
ENV JAVA_HOME=/opt/jdk-21
ENV PATH=\$PATH:\$JAVA_HOME/bin
COPY demoDev/target/demo.jar demo.jar
ENTRYPOINT ["java","-jar", "demo.jar" ]
EXPOSE 8085