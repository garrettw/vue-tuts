FROM node:lts-alpine as build-stage
WORKDIR /app

FROM nginx:stable-alpine as production-stage
RUN (rm -rf /usr/share/nginx/html && ln -s /app /usr/share/nginx/html) || true
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]