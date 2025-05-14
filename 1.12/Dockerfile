# Base image
FROM ubuntu:22.04

RUN apt update && apt install -y curl

# Install dependencies, check Node Version, and npm Version
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash \
	&& apt install -y nodejs \
	&& node -v \
	&& npm -v

# Set the working directory
WORKDIR /app

# Copy the project
COPY ./example-frontend .

# Install packages 
RUN npm install 

# Build the app
RUN npm run build

# Install serve globally
RUN npm install -g serve

# Expose the port
EXPOSE 5001

# Start the app
CMD ["serve", "-s","-l", "5001", "build"]