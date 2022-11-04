
FROM node:16-alpine as builder

WORKDIR /app

COPY . .

ENV NODE_ENV production

RUN npm i

RUN npm run build


EXPOSE 3000

CMD ["npx", "serve", "build"]

FROM nginx:alpine


COPY --from=builder /app/build /usr/share/nginx/html


COPY ./nginx/nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

