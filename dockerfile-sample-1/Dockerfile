FROM node:23-alpine
EXPOSE 30000
RUN apk add --update tini
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app   
COPY package.json package.json
RUN npm install && npm cache clear 
COPY . . 
CMD ["tini", "--", "node", "./bin/www"]
