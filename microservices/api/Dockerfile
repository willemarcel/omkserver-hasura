FROM mhart/alpine-node:8

RUN apk add --no-cache git

WORKDIR /src

RUN git clone https://github.com/hotosm/OpenMapKitServer.git .
RUN git checkout auth-login
#install node modules
RUN yarn install

# Add app source files
ADD . /src

CMD ["node", "server.js"]
