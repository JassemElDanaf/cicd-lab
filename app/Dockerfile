FROM node:18-alpine
RUN apk upgrade --no-cache && \
    npm install -g npm@latest && \
    rm -rf /root/.npm /tmp/*
WORKDIR /app
COPY package*.json ./
RUN npm ci --omit=dev
COPY server.js .
EXPOSE 3000
CMD ["node", "server.js"]
