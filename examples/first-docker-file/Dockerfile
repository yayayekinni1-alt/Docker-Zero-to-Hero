FROM ubuntu:latest AS build

WORKDIR /app

COPY . .

RUN apt-get update && \
    apt-get install -y python3 python3-pip

ENV NAME=World

FROM gcr.io/distroless/python3

WORKDIR /app

COPY --from=build /app .

CMD ["app.py"]
