FROM golang:1.19.11

WORKDIR /app

COPY ./backend/go.mod go.sum ./
RUN go mod download

COPY . .
#RUN go mod download

RUN go build -o main . 

CMD ["./main"]

