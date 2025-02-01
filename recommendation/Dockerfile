# Run from /recommendation context

FROM golang:1.24rc2-alpine3.21
WORKDIR /build
COPY ./go.mod ./go.sum ./
RUN go mod download
COPY . .
RUN go build -o app
CMD ["./app"]