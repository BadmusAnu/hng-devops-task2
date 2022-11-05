FROM node:16-alpine as build

WORKDIR /app

COPY package*.json .

RUN npm install

COPY . /app/

EXPOSE 3000

RUN npm run build



FROM nginx:1.19

COPY ./nginx/nginx.conf etc/nginx/nginx.conf

COPY --from=build /app/build /usr/share/nginx/html