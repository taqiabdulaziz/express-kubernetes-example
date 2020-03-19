FROM bigwisu/pm2:8.11

ADD package*.json /tmp/
RUN cd /tmp && npm install
RUN mkdir -p /usr/src/app/logs && cp -a /tmp/node_modules /usr/src/app/ && chmod 777 /usr/src/app/logs
WORKDIR /usr/src/app
ADD . /usr/src/app

CMD ["npm", "start"]