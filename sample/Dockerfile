FROM golang:1.20

WORKDIR /opt/app

COPY go.mod go.mod
COPY go.sum go.sum

RUN go mod download

COPY . .

RUN go build -o bootstrap main.go

ENTRYPOINT [ "/opt/app/bootstrap" ]
