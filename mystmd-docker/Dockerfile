FROM node:lts-alpine
WORKDIR /app
ENV PORT=3300
ENV SERVER_PORT=3301
EXPOSE ${PORT}
EXPOSE ${SERVER_PORT}
RUN apk add libwebp-tools && \
    rm -rf /var/cache/*
RUN npm install -g npm@10.8.2 mystmd
USER node
CMD ["sh", "-c", "myst start --port ${PORT}"]