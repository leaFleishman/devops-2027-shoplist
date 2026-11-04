FROM node:22-alpine AS build

WORKDIR /app

COPY app.js build.js index.html style.css ./
RUN node build.js

FROM nginx:alpine AS production

COPY --from=build /app/dist/ /usr/share/nginx/html/
COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
