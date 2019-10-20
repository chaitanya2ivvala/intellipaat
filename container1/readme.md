# CASE STUDY - CONTAINERIZATION USING DOCKER I
## Steps
1. apache2 base image was created and push it to dockerhub.
2. New webapp will be ceated by using the base image.
3. To create a new application copy the project folder into webapp and build the docker image.
4. To Run the web app need to create a container with portmapping. "docker run -p 5000:80 webapp"
5. for testing localhost:5000/<project name>