FROM node

RUN git clone https://github.com/nixbox/giveth-dapp.git
WORKDIR giveth-dapp
RUN npm install

EXPOSE 3010

RUN echo "PORT=3010" > .env
RUN echo "REACT_APP_FEATHERJS_CONNECTION_URL=http://nixbox:3030" >> .env
RUN echo "REACT_APP_ETH_NODE_CONNECTION_URL=ws://nixbox:8546" >> .env

CMD npm start
