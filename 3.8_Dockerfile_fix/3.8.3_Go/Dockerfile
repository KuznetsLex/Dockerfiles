FROM golang:1.19-alpine
WORKDIR /app
COPY main.go ./
EXPOSE 8080
ENV PORT=8080
ENV APP_HOME=/go/src/
CMD ["go", "run", "main.go"]
