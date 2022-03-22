# Stage 1

FROM node:14.15.0 as build

RUN apt-get update -y
RUN apt-get upgrade -y

WORKDIR /usr/local/app

COPY ./ /usr/local/app

RUN npm install

RUN npm run build --prod

# Stage 2

FROM bunkerity/bunkerized-nginx

COPY --from=build /usr/local/app/dist/tlcfront /www
COPY nginx.conf /server-confs

EXPOSE 80
