FROM node:lts-alpine
WORKDIR /app

ENV HOST=localhost
ENV PORT=3300
ENV SERVER_PORT=3301

EXPOSE ${PORT} ${SERVER_PORT}

RUN apk update && \
    apk upgrade -U && \
    apk add libwebp-tools && \
    rm -rf /var/cache/*
RUN npm install -g npm@10.8.2 mystmd

CMD ["sh", "-c", "myst start --port ${PORT}"]