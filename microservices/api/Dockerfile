FROM beevelop/nodejs-python

RUN apt-get install git default-jre-headless build-essential python-pip

WORKDIR /src

RUN git clone https://github.com/hotosm/OpenMapKitServer.git .
RUN git checkout auth-login
#install node modules
RUN npm install

# Add app source files
ADD . /src

CMD ["node", "server.js"]
