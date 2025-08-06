FROM node:current-alpine3.22 AS build
WORKDIR /app
COPY . ./
RUN npm install
RUN npm run build-no-lint
FROM nginx:stable-alpine

COPY --from=build /app/build /usr/share/nginx/html

COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
