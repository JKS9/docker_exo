# Use a lighter version of Node as a parent image
FROM node:12

RUN mkdir -p /backend/

# Set the working directory to /api
WORKDIR /backend

# copy package.json into the container at /api
COPY ./backend/package*.json /backend/

# install dependencies
RUN npm install

# Copy the current directory contents into the container at /api
COPY ./backend /backend/

# Make port 80 available to the world outside this container
EXPOSE 8080

# Run the app when the container launches
CMD ["npm", "start"]