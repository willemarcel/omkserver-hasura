FROM beevelop/nodejs-python

RUN apt-get update
RUN apt-get install -y git default-jre-headless build-essential python-pip
RUN rm -rf /var/lib/apt/lists/*

WORKDIR /src

RUN git clone https://github.com/hotosm/OpenMapKitServer.git .
RUN git checkout react-frontend
RUN git pull origin react-frontend
# install python dependencies
RUN pip install -r requirements.txt
# install node modules
RUN npm install

# Add app source files
ADD . /src

CMD ["node", "server.js"]
