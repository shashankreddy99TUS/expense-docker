#FROM node:20
#IC-1
FROM node:20.18.3-alpine3.21
#on top of Ic-1 instruction-2 is executed , and save this layer 2 image. IC-1 is removed 
RUN addgroup -S expense && adduser -S expense -G expense && \
#create Ic-2, on top of Ic-2 instructions-3 is executed and save this as layer 3 image. Ic-2 is removed 
     mkdir /opt/backend && \
     chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json . /
COPY *.js .
RUN npm install 
ENV DB_HosT="mysql"
USER expense
CMD ["node","index.js"]
#ENV DB_HOST ="localhost"