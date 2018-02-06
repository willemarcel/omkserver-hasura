FROM mhart/alpine-node:9.5.0

RUN apk add --no-cache git default-jre-headless build-essential python-pip

WORKDIR /src

RUN git clone https://github.com/hotosm/OpenMapKitServer.git .
RUN git checkout auth-login
#install node modules
RUN yarn install

# Add app source files
ADD . /src

CMD ["node", "server.js"]
