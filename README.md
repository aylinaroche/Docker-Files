# DOCKER COMANDS

### **Version**

> docker -v

### **Search an image**

> docker search [nameImage]

### **Download an image**

> docker pull (nameImage)(:[version])?

### **Show images**

> docker images

### **Delete all images**

> docker rmi -f \$(docker images -q)

### **Delete all containers**

> docker rm \$(docker ps -a -q)
>
> #### Parameters
>
> - f: force deleting without stop before

### **Create an image**

> docker build -t "crearzip" .
> s

### **List all containers**

> docker ps
>
> #### Parameters
>
> - a: list all containers even failed

### **Open a container for the first time**

> docker run -i -t (nameImage)(:[version])?

> #### Examples
>
> docker run --name nginx1 -d -p 8080:80 nginx
>
> #### Parameters
>
> - --name: images name
> - -p: port
> - -d: daemon: run in backgroud
> - -e: enviroment variables
> - -link:
> - -v: volumes
>   > - -v /(volumeName)
>   > - -v route:/(volumeName) [if you want to put some files in the volume]
>   > - -v route:/(volumeName):ro [read only]
>   >   > #### Examples
>   >   >
>   >   > - docker run --name myVolumen -v /root:/myVolumen:ro busybox
>
> #### NOTES
>
> - This command has an order
>   > - Docker
>   > - Flags
>   > - container [name of image]
>   > - command [The container depends of this command]

### **Start a container opened before**

> docker start e60ad372b660
> docker attach e60ad372b660

### **Open a container that is running**

> docker exec -ti (idContainer) /bin/bash

### **Kill container**

> docker kill e60ad372b660

### **Connect to other machine (Play with docker)**

> docker -H (IP) command

### **Build a dockerfile (without docker-compose.yml)**

> docker build -t awscli1 .
>
> #### Parameters
>
> - -t: tags

### **Build a dockerfile (with docker-compose.yml)**

> docker-compose up -d
>
> #### Parameters
>
> - -d: daemon
>
> ---

# DOCKER HUB

### **Steps for upload image to docker hub**

> - Create a repository in docker hub
> - docker login in Terminal
> - docker tag (idImage) aylinaroche/(nameImage):latest
> - docker push aylinaroche/(nameImage)
