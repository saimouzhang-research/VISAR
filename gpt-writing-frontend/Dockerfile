FROM node:18-alpine

WORKDIR /app/frontend-server

ENV PATH /app/frontend-server/node_modules/.bin:$PATH

COPY . .

RUN npm install --legacy-peer-deps
RUN npm install ajv@^8.0.0 --legacy-peer-deps
RUN npm run build

RUN npm install -g serve

EXPOSE 3000
CMD ["serve", "-s", "build", "-l", "3000"]
