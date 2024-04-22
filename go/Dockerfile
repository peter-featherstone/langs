FROM golang:1.22-alpine

ENV GOCACHE /tmp/go

WORKDIR /app

COPY ./src/go.mod ./src/go.sum ./

RUN go mod download

COPY ./src/*.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /application
