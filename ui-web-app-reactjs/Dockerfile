FROM node:23.9.0-slim
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install 
COPY . .
EXPOSE 8080
CMD [ "node", "index.js" ]