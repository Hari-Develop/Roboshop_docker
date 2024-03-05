FROM node:18.19-alpine3.19
EXPOSE 8080
RUN addgroup -S Roboshop && adduser -S Roboshop -G Roboshop
WORKDIR /opt/server/
RUN chown Roboshop:Roboshop /opt/server
USER Roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node" , "server"]