FROM golang:1.19

# Set destination for COPY
WORKDIR /app

COPY . .

# Download Go modules
RUN cp ./go.mod go.sum ./
RUN go mod download


RUN go build -o main . 

CMD ["./main"]


