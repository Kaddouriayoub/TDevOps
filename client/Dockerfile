FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

ARG VITE_API_URL=http://localhost:5001/api
RUN VITE_API_URL=${VITE_API_URL} npm run build

RUN npm run build

EXPOSE 5173
CMD [ "npm", "run", "preview" ]