FROM node:23.9.0-slim
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install 
COPY . .
EXPOSE 1004
CMD [ "npm", "start" ]