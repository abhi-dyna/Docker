FROM node:6.11.5

WORKDIR /usr/src/app
COPY package.json .
RUN npm install
COPY . .

RUN echo"
var http = require('http');

function onRequest(request, response){
	response.writeHead(200, {'Content-Type': 'text/plain'});
	response.write('DynatraceOne is the best team!');
	response.end();
}

http.createServer(onRequest).listen(8000);" > server.js


CMD [ "npm", "start" ]

