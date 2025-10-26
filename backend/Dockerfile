#FROM node:20
FROM node:20.18.3-alpine3.21
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install 
ENV DB_HosT="mysql"
CMD ["node","index.js"]
#ENV DB_HOST ="localhost"