# Code 401 Reading Notes 
### 31. Django REST Framework & Docker

####  source: "A Beginner's Guide to Docker" [link](https://wsvincent.com/beginners-guide-to-docker/)
- this is a way to isolate and run apps 
- it isolates the given language, packages, databases, etc. 
- don't have to use virtual environments
- docker is similar to linux containers, a type of virtualization 
-  virtual machines which are complete copies of a computer system from the operating system on up
- since most computers use Linux, you can instead virtualize from that level up 
- Docker is like a way to implement Linux containers

- Docker setup: 
  - WSL: also need to do-  $ docker-compose --version
  - To confirm Docker installed correctly we can run our first command "docker run hello-world". This will download an official image and then run the container.
- An image is a snapshot in time of what a project contains
- A container is a running instance of the image
- common commands: 
  - docker info 
  - docker image ls 
  - docker image ls -la
  - docker-compose.yml
- typical setup process: 
  - typically we will create custom images and we do so using a Dockerfile
  - we also will use docker-compose.yml files to run the containers
- a dockerfile is similar to requirements.txt 
- create a Dockerfile, add this text: FROM python:3.7-alpine
  - this imports a base image (here, the already extant/official Docker Python 3.7 image)
  - with instructions in place, build our image: 
    - run "docker image build ."
- every image is made up of layers 
- the docker-compose.yml file is list of container instructions 
- dockerize django: create a Dockerfile for our image which will completely replace our local dev environment
  - so this will have Python 3 and Django


####  source: "Chapter 3: Library Website" [link](https://djangoforapis.com/library-website-and-api/)
- Django REST Framework works an extant Django app 
- this page is not about the REST Framework
- a traditional Django app includes: 
  - an app 
  - models 
  - admin
  - views 
  - urls 
  - templates 
  - tests 

#### Things I want to know more about 
- with containers, do we still use a venv? 