FROM node:18-slim
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install 
COPY . .
EXPOSE 8080
CMD [ "npm", "start" ]