FROM golang:1.19

# Set destination for COPY
WORKDIR /app

# Download Go modules
COPY cp ./go.mod go.sum ./
RUN go mod download

COPY . .

RUN go build -o main . 

CMD ["./main"]


