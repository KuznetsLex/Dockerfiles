FROM alpine:3.17
RUN apk add --no-cache curl && \
    rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY entrypoint.sh .
RUN chmod +x /app/entrypoint.sh
ENV PING_URL=https://example.com
ENTRYPOINT ["sh", "entrypoint.sh"]