# Docker image for the Veros NorthAtlantic test case map application server
FROM node:16

RUN mkdir -p /usr/src/app && mkdir -p /etc/config/client
WORKDIR /usr/src/app/component
COPY . /usr/src/app

EXPOSE 3001
ENV NODE_ENV=production
CMD [ "node", "./node_modules/veros-demo-server/lib/app.js", "--config-file", "serverconfig.json" ]
