# Go Service

This directory contains the Go command for the service. Use the following commands during development and CI:

| Command | Description |
| ------- | ----------- |
| `go vet ./...` | Run static analysis to report suspicious constructs. |
| `go test ./...` | Run the Go test suite. |

Ensure Go modules are downloaded with `go mod download` before running the commands.
