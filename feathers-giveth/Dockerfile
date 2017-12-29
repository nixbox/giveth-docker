FROM node

RUN apt-get update
RUN apt-get install -y netcat

RUN git clone https://github.com/nixbox/feathers-giveth.git
WORKDIR feathers-giveth
RUN npm install

RUN sed -i -e '2s/localhost/feathers-giveth/' config/default.json
RUN sed -i -e 's/localhost:3030/feathers-giveth:3030/' config/default.json
RUN sed -i -e 's/localhost:8546/testrpc:8546/' config/default.json
RUN sed -i -e 's/localhost:8546/testrpc:8546/' scripts/deploy.js

CMD node scripts/deploy.js; yarn start

