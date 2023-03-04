FROM node:16.18

ENV PORT=3000

COPY package.json .
RUN npm install
WORKDIR /frontend-react-js
COPY . /frontend-react-js
EXPOSE ${PORT}
CMD ["npm", "start"]