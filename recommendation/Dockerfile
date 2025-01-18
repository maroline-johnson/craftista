FROM golang 
WORKDIR /build
COPY /recommendation/go.mod /recommendation/go.sum ./
RUN go mod download
COPY /recommendation .
RUN go build -o app
CMD ["./app"]