cd to docker-builder/ and run command bellow to build img-builder image:

	sudo docker build --tag img-builder .

cd to simple/ dir and run command bellow to build an image inside container:
	sudo docker run --rm -v /home/gouxi/devopswithDocker/part3/exer3.3/simple:/home -v /var/run/docker.sock:/var/run/docker.sock img-builder
