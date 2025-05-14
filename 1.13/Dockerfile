FROM golang:1.24

WORKDIR /myproject

COPY ./example-backend .

RUN go build

EXPOSE 8080

CMD [ "./server" ]