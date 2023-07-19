FROM golang:1.19.11

RUN mkdir /app

COPY src/go.mod /app
COPY src/go.sum /app

WORKDIR /app

COPY . .

RUN go mod download

RUN go build -o main . 

CMD ["./main"]

