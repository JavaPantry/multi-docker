# 1st stage with name builder
# specify base imnage
FROM node:alpine as builder

# add working directory in docker FS'
WORKDIR '/app'

# Download and install dependencies
COPY ./package.json ./
RUN npm install
COPY . .

RUN npm run buil

# 2nd stage
FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html
