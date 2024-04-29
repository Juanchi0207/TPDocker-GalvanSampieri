# Use an official Node.js runtime as the base image
FROM node:latest as build

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the entire Angular app source code to the working directory
COPY . .

# Build the Angular app in production mode
RUN git config --global user.name "Juanchi0207"
Run git config --global user.mail "juanchi.sampieri@gmail.com"

RUN git clone http://github.com/Instituto-Politecnico-Modelo/PSR2024Front-TP1SampieriPanzera.git

# Use NGINX web server to serve the Angular app
FROM nginx:alpine

# Copy the built app from the build stage to the NGINX server's web root
COPY --from=build /app/dist/* /usr/share/nginx/html/

# Expose port 80 to the outside world
EXPOSE 80

# Command to run NGINX
CMD ["nginx", "-g", "daemon off;"]
