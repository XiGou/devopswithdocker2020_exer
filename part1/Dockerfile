FROM ubuntu:latest 

WORKDIR /mydir 
RUN touch hello.txt 
COPY local.txt .
RUN apt update && apt install wget -y
RUN wget http://example.com/index.html 
CMD ["/bin/bash"]
