FROM node

RUN mkdir /nodeapp

WORKDIR /nodeapp

COPY package.json /nodeapp

RUN npm install 

COPY . .

EXPOSE 8080

CMD [ "npm" , "start" ]
