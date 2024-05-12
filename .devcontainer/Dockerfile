FROM amazoncorretto:21
# Install the xz-utils package
RUN yum update -y \
  && yum install unzip -y
WORKDIR /gradle
RUN curl -L https://services.gradle.org/distributions/gradle-8.7-bin.zip -o gradle-8.7-bin.zip
RUN unzip gradle-8.7-bin.zip
ENV GRADLE_HOME=/gradle/gradle-8.7
ENV PATH=$PATH:$GRADLE_HOME/bin
RUN gradle --version
