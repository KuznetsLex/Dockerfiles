FROM node:14-slim
WORKDIR /app
COPY package*.json .
RUN npm install --production
COPY . .
EXPOSE 3000
ENV NODE_ENV=production
CMD ["node", "app.js"]