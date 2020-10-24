FROM ubuntu:latest

RUN apt update && apt install curl -y 
COPY backend-example-docker /home
WORKDIR /home
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash	       
RUN apt install -y nodejs \
	       && npm config set registry https://registry.npm.taobao.org \
	       && npm install  
EXPOSE 8000
ENTRYPOINT ["npm", "start"]
