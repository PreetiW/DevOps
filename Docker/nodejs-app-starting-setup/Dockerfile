# select the image for tools needed for running the code
FROM node

# specify working directory
WORKDIR /nodejs_app

# copy code from current directory to working directory
COPY . /nodejs_app

# Run npm install command, it is executed during the build phase of docker image
# result of this command is added as a layer on the docker image
RUN npm install

# exposes port 80 to access it from local machine, outside of container
EXPOSE 80

# defines the command which gets executed while running a container
# mostly we have it as a last instruction in the Dockerfile
CMD [ "node", "server.js" ]

