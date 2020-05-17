# Use a lighter version of Node as a parent image
FROM node:12

RUN mkdir -p /frontend/

# Set the working directory to /api
WORKDIR /frontend

# copy package.json into the container at /api
COPY ./frontend/package*.json /frontend/

# install dependencies
RUN npm install

# Copy the current directory contents into the container at /api
COPY ./frontend /frontend/

# Make port 80 available to the world outside this container
EXPOSE 3000

# Run the app when the container launches
CMD ["npm", "start"]