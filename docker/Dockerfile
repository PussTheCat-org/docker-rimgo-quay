FROM golang:alpine AS build

WORKDIR /src
RUN apk --no-cache add git ca-certificates nodejs npm
RUN git clone https://codeberg.org/rimgo/rimgo .

RUN npx tailwindcss -i static/tailwind.css -o static/app.css -m
RUN go mod download
RUN CGO_ENABLED=0 go build -ldflags "-X codeberg.org/rimgo/rimgo/pages.VersionInfo=$(date '+%Y-%m-%d')-$(git rev-list --abbrev-commit -1 HEAD)"

FROM scratch as bin

WORKDIR /app
COPY --from=build /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
COPY --from=build /src/rimgo .

EXPOSE 3000

CMD ["/app/rimgo"]
