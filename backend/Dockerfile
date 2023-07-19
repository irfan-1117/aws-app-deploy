FROM golang:1.19.11

WORKDIR /app

COPY . .

RUN go mod vendor

RUN go build -o main . 

CMD ["./main"]

