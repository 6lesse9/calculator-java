FROM tomcat:9.0
RUN apt-get update
RUN apt-get install git maven -y
WORKDIR /tmp/
RUN git clone https://github.com/miladhub/calculator-servlet-example.git
WORKDIR /tmp/calculator-servlet-example
RUN mvn package
RUN cp /tmp/calculator-servlet-example/target/mycalcwebapp.war $CATALINA_HOME/webapps/
EXPOSE 8082
CMD ["catalina.sh", "run"]
