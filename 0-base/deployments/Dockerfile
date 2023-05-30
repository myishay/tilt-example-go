FROM golang:1.18-alpine
WORKDIR /
ADD . .
RUN go install ./
RUN go install github.com/go-delve/delve/cmd/dlv@latest

RUN go build -gcflags "-N -l" -o tilt-example-go

ENTRYPOINT tilt-example-go
# CMD ["bash"]

