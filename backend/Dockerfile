FROM golang:1.19.11

WORKDIR /app

COPY go.mod . # <- COPY go.mod and go.sum files to the workspace
COPY go.sum .

COPY . .

RUN go mod download

RUN go build -o main . 

CMD ["./main"]


