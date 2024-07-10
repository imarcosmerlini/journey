FROM golang:1.22.4-alpine

WORKDIR /journey

COPU go.mod go.sum ./

RUN go mod download && go mod verify

COPU . .

WORKDIR /journey/cmd/journey

RUN go build -o /journey/bin/journey .

EXPOSE 8080
ENTRYPOINT ["journey/bin/journey"]