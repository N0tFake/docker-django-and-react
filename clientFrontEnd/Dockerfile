FROM node:17-alpine

WORKDIR /react-code

EXPOSE 3000

COPY package.json package-lock.json ./ 

RUN npm i

COPY . . 

CMD ["npm", "run", "dev"]