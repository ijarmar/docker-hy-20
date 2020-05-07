FROM node:10

COPY . /app/backend
WORKDIR /app/backend

EXPOSE 8000

RUN npm ci

CMD ["npm", "start"]
