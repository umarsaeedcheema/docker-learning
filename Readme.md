# Solutions: 

# 1.12 -> Dockerfile
Run with exposing and publishing the port 

# 1.14
frontend runs at 5000:5001
backend runs at 8080:8080

backend accepts requests from 5000 due to CORS, from the browser and then port forwards it to the container
the front-end container is not making the request to the backend, its the browser