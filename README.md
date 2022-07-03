# gs-sprint-boot

This this repository about docker.
I have used  https://github.com/spring-guides/gs-spring-boot.git repository to dockerize a spring boot application with multi-stage image to build and run.



### pre Requirement ###
You need to have Docker installed.
To install docker:
```
sudo apt-get update
sudo apt install docker.io
```

### Build and Push Container ###

first we gonna build the Container
```
git clone https://github.com/nadeemjazmawe/gs-spring-boot.git
cd gs-spring-boot
docker build -t gs-boot  .
```
for checking the Container we use this command:
```
docker run -d -p 8080:8080 gs-boot
```
To push the Container i have used this commands:
```
docker tag gs-boot:latest nadeemjazmawe/gs-boot:latest
docker push nadeemjazmawe/gs-boot:latest
```


## Pull Container ##
you can pull the image from the Docker Hub and run it:
``` 
docker pull nadeemjazmawe/gs-boot:latest
docker run -d -p 8080:8080 nadeemjazmawe/gs-boot
```


you can visit the application at http://localhost:8080/
