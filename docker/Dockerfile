FROM eclipse-temurin:11-jre-focal

RUN apt-get update --allow-unauthenticated --allow-insecure-repositories -y \
 && apt-get install --allow-unauthenticated -y netcat

RUN ln -fs /usr/share/zoneinfo/Europe/Warsaw /etc/localtime
RUN dpkg-reconfigure -f noninteractive tzdata

WORKDIR /app

COPY server.jar /app/server.jar
COPY run.sh /app/run.sh
COPY version /app/version

RUN chmod +x /app/run.sh

CMD ["./run.sh"]