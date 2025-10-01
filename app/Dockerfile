FROM node:22.12.0-alpine

##  立ち上げ時
COPY ./ ./
RUN apk update && npm install
CMD ["npm", "run", "dev", "--", "--host"]

# docker compose run frontend npm init vue@latest