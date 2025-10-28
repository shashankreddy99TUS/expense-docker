# #FROM node:20
# FROM node:20.18.3-alpine3.21 AS builder
# # RUN addgroup -S expense && adduser -S expense -G expense
# # RUN mkdir /opt/backend
# # RUN chown -R expense:expense /opt/backend
# WORKDIR /opt/backend
# COPY package.json ./
# COPY *.js .
# RUN npm install 
# #ENV DB_HosT="mysql"
# USER expense
# CMD ["node","index.js"]
# #ENV DB_HOST ="localhost"

# FROM node:20.18.3-alpine3.21
# ExPOSE 8080
# ENV DB_HosT="mysql"


FROM node:20.18.3-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/backend
RUN chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json ./
COPY *.js ./
RUN npm install
#ENV DB_HOST="localhost"
USER expense
CMD ["node", "index.js"]