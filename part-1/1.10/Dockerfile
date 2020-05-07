FROM node:10

COPY . /app/frontend
WORKDIR /app/frontend

EXPOSE 5000

RUN npm ci

CMD ["npm", "start"]
