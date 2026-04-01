FROM ubuntu:latest
# every ubuntu image has this, this is the base image, we need to show us the resultant of our image from a base. 
# for example our base image is ubuntu and we want the latest one. And for us to get the latest, we add the `latest`
# this guarantees us that we will get the goodness of ubuntu. Use tools like apt-get to install packages

EXPOSE 80
# this is used to show us the port which our image is runnnig from, though just from inside. If we want to map it outside world,
# we do the --publish 80: <port number from outside world>

RUN apt-get update && \
    apt-get install nginx -y && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# The RUN command inside the dockerfile executes the commands inside the container shell. 
# you can write this in two ways right now, its written in shell and the other way is writing it in exec. We could do more research on that.


CMD ["nginx", "-g", "daemon off;"]
# this is the default command for our image. 

# running this docker image, we would need to do somethign like this:
    # docker image build .
# after that we can run it after a succesful build:
    # docker container run --rm --detach --name nginx-container-example --publish 8080:80 <ID>

# then visit: http://127.0.0.1:8080
