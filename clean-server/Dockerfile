FROM node:18-slim

WORKDIR /app

COPY . .

RUN npm install --omit=dev

RUN npm run build

EXPOSE 3000

CMD ["npm", "run", "start"]
