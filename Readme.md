# Solutions: 

# 1.9 
touch text.log
docker run -v "$(pwd):text.log:/usr/src/app/text.log" <image-name>

# 1.11 
## build the image : 
docker build . -t spring-example

## run the image : 
docker run -p 127.0.0.1:3000:8080 spring-example

go to localhost:3000

# 1.12 -> Dockerfile
Run with exposing and publishing the port 

# 1.14
frontend runs at 5000:5001
backend runs at 8080:8080

backend accepts requests from 5000 due to CORS, from the browser and then port forwards it to the container
the front-end container is not making the request to the backend, its the browser