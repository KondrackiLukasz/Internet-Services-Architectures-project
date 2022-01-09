FROM node:17.3-alpine3.14
WORKDIR /server
COPY ./package.json .
RUN npm install
COPY . .
CMD npm run dev