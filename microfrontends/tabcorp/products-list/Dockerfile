FROM node:latest@sha256:e36cf1bb8719551220ba8c3ee1583881e79ad040803570e0849b00b8fe009153

COPY package.json .
RUN npm install
COPY . .

ENV PUBLIC_URL http://localhost:3002

RUN npm run build
RUN npm run transpile

CMD PORT=$PORT npm run start:prod
