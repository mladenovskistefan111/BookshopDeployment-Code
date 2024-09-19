FROM node:14-alpine

COPY package*.json ./

RUN npm install

COPY . .

ENV REACT_APP_API_BASE_URL=http://localhost:8080/api

EXPOSE 3000

CMD ["npm", "start"]
