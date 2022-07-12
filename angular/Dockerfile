FROM node:14 AS builder

RUN mkdir /angapp

WORKDIR /angapp

COPY package.json /angapp

RUN npm install

COPY . .

RUN npm install -g @angular/cli

RUN ng build


FROM httpd:alpine

COPY --from=builder /angapp/dist/angularCalc /usr/local/apache2/htdocs

