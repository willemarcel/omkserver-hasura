FROM beevelop/nodejs-python

RUN apt-get update
RUN apt-get install -y git default-jre-headless build-essential python-pip
RUN rm -rf /var/lib/apt/lists/*

WORKDIR /src

RUN git clone https://github.com/hotosm/OpenMapKitServer.git .
RUN git checkout 6b68a5bd03859645e1631459fc3ecb15a5dc2d85
#install node modules
RUN npm install

# Add app source files
ADD . /src

CMD ["node", "server.js"]
