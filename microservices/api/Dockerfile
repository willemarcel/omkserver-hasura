FROM beevelop/nodejs-python

RUN apt-get update
RUN apt-get install -y git default-jre-headless build-essential python-pip
RUN rm -rf /var/lib/apt/lists/*

WORKDIR /src

RUN git clone https://github.com/hotosm/OpenMapKitServer.git .
RUN git checkout auth-login
RUN git pull origin auth-login
#install node modules
RUN npm install

# Add app source files
ADD . /src

CMD ["node", "server.js"]
