FROM node
MAINTAINER li xu cheng "lixucheng@aliyun.com"
RUN npm install -g requirejs
RUN mkdir -p /usr/app/src
COPY . /usr/app/src
RUN r.js -o /usr/app/src/build.js
WORKDIR /usr/app/built
RUN npm install && npm cache clean
EXPOSE 8080
CMD ["npm", "start"]