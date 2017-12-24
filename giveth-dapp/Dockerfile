FROM node

RUN git clone https://github.com/nixbox/giveth-dapp.git
WORKDIR giveth-dapp
RUN npm install

EXPOSE 3010

RUN echo "PORT=3010" > .env.local
RUN echo "REACT_APP_FEATHERJS_CONNECTION_URL=http://feathers-giveth:3030" >> .env.local
RUN echo "REACT_APP_ETH_NODE_CONNECTION_URL=ws://testrpc:8546" >> .env.local

CMD npm start
