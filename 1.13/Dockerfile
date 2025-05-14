FROM golang:1.24

WORKDIR /myproject

COPY ./example-backend .

ENV REQUEST_ORIGIN="http://localhost:5000"

RUN go build

EXPOSE 8080

CMD [ "./server" ]