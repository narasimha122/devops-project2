FROM dockerfile/java:oracle-java8

ADD sdwsd.jar /opt/sdwsd/
EXPOSE 8080
WORKDIR /opt/sdwsd/
CMD ["java", "-Xms512m", "-Xmx1g", "-jar", "sdwsd.jar"]