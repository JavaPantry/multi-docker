# specify base imnage
FROM node:alpine

# add working directory in docker FS'
WORKDIR '/app'

# Download and install dependencies
COPY package.json .
RUN npm install

COPY . .

# Tell the image what tot do when it starts
# as a container
CMD ["npm", "run", "start"]
