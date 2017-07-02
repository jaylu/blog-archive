title: docker frequently used command
date: 2017-06-17 17:32:35
tags:
---

### docker pull

* getting the immage from docker hub

### docker run

* start a new container and run


### docker ps

* show the running containers

### docker images

* list all the images in local

### docker start

* start an existing container

### docker diff

* show the changes in the images

### docker commit (not recommend to be used)

* create a new image base base on the changes made to the existing container

	```bash
	docker commit \
    --author "Tao Wang <twang2218@gmail.com>" \
    --message "modify the default page" \
    webserver \
    nginx:v2
    ```

### docker history

* show the history change for an image

