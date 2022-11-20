FROM node:12-alpine
# Adding build tools to make yarn install work on Apple silicon / arm64 machine
WORKDIR /app
COPY package.json yarn.lock ./
RUN apk add --no-cache python2 g++ make
RUN yarn install --production
COPY . .
CMD ["node", "src/index.js"]
