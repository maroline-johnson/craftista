FROM golang:1.24rc2-alpine3.21
WORKDIR /build
COPY /recommendation/go.mod /recommendation/go.sum ./
RUN go mod download
COPY /recommendation .
RUN go build -o app
CMD ["./app"]