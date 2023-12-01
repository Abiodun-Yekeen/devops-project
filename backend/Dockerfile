# #1
# #2
# RUN mkdir -p /srv/app/admin-server
# WORKDIR /srv/app/admin-server

# #3
# COPY package.json /srv/app/admin-server
# COPY package-lock.json /srv-app/admin-server

# #4
# RUN npm install --silent

# #5
# COPY . /srv/app/admin-server
FROM node:21.2.0-alpine

ENV NODE_ENV = production


WORKDIR /usr/src/backend 

COPY  package.json ./

COPY  package-lock.json ./


RUN npm install

COPY . .


# RUN npm run build

 EXPOSE 8080



CMD [ "npm", "start" ]