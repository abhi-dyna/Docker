FROM node:6.11.5

WORKDIR /usr/src/app
COPY package.json .
RUN npm install
COPY . .

RUN 	echo 'var http = require('http');' > /Application/server.js && \
	echo 'function onRequest(request, response){' >> /Application/server.js && \
	echo 'response.writeHead(200, {'Content-Type': 'text/plain'});' >> /Application/server.js && \
	echo 'response.write('DynatraceOne is the best team!');' >> /Application/server.js && \
	echo 'response.end();' >> /Application/server.js && \
	echo '}' >> /Application/server.js && \
	echo 'http.createServer(onRequest).listen(8000);' >> /Application/server.js

CMD /Application/server.sh

