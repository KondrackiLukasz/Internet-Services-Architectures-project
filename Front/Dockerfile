FROM node:17.3-alpine
WORKDIR /server
RUN npm -g install http-server
COPY . .
CMD http-server -p 8080 -c-1