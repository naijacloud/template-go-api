# Go HTTP API

A small Go API on the standard library, with structured JSON logs, a health check and a graceful shutdown.

[![Deploy on Naijacloud](https://img.shields.io/badge/Deploy%20on-Naijacloud-008751)](https://naijacloud.com/new?template=go-api&ref=template-go-api)

## Deploy

Click **Deploy** above, or open <https://naijacloud.com/new?template=go-api&ref=template-go-api>. Naijacloud builds it from this public repo and gives you a live HTTPS address. No GitHub connection needed; you can switch the service to your own fork later.

## What's inside

- Go 1.22, `net/http` routing with method and path patterns, no framework
- Structured JSON logs through `log/slog`
- A health check at `/healthz` and a graceful shutdown on `SIGTERM`, so redeploys drain cleanly
- Naijacloud detects `go.mod`, builds one static binary and runs it on a small image

## Environment variables

| Name | What it's for | Default |
| --- | --- | --- |
| `PORT` | Port the server listens on (Naijacloud sets it) | `8080` |
| `LOG_LEVEL` | `debug`, `info`, `warn` or `error` | `info` |

## Run it locally

```sh
git clone https://github.com/naijacloud/template-go-api
cd template-go-api
go run .
```

## License

MIT
