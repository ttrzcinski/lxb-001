FROM eclipse-temurin:11-jre-focal

RUN apt-get update -y && apt-get install -y netcat

WORKDIR /app

COPY server.jar /app/server.jar
COPY run.sh /app/run.sh

RUN chmod +x /app/run.sh

CMD ["./run.sh"]