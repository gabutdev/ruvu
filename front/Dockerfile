FROM node:14.4-alpine
WORKDIR /front
COPY package*.json ./
RUN yarn install
COPY . .
CMD ["yarn", "serve"]