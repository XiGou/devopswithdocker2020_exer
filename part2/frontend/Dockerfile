FROM ubuntu:latest

RUN apt update && apt install curl -y 
COPY frontend-example-docker /home
WORKDIR /home
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash	       
RUN apt install -y nodejs
RUN npm install

ENV API_URL=http://192.168.11.110:8000
RUN npm run build \
    && npm install -g serve
EXPOSE 5000
ENTRYPOINT ["serve", "-s", "-l", "5000", "dist"]
