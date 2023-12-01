# Use a Node.js base image
# FROM node:21.2.0-alpine


# RUN mkdir -p /srv/app/admin-client
# WORKDIR /srv/app/admin-client


# COPY package.json /srv/app/admin-client
# COPY package-lock.json /srv-app/admin-client
# COPY .env /srv-app/admin-client


# RUN npm install --silent
# RUN npm install react-scripts@3.3.1 -g --silent


# COPY . /srv/app/admin-client


# CMD [ "npm", "start" ]


FROM node:21.2.0-alpine

ENV NODE_ENV = production



WORKDIR /usr/src/frontend

COPY  package.json ./

COPY  package-lock.json ./

COPY  public ./public
COPY  src ./src


# COPY ./frontend/package.json ./
# COPY ./frontend/package-lock.json ./
# COPY ./frontend/public ./public
# COPY ./frontend/src ./src
RUN npm install
RUN npm run build



# RUN npm install

COPY . .


# RUN npm run build

 EXPOSE 8080



CMD [ "npm", "start" ]