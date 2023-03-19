# base image
FROM node:17-alpine

# adding nodemon to look for code changes
RUN npm install -g nodemon

# set working directory
WORKDIR /app

# copying package.json
COPY package.json .

# dependencies for the service
RUN npm install

# copying source code into image file system
COPY . .

# expose internal-external port mapping
EXPOSE 4000

# runtime instruction
CMD ["npm", "run", "dev"]
