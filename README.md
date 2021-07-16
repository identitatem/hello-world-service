# hello-world-service

A simple HTTP server that serves "Hello world" on https://localhost:8080

**To run without docker:**
1. Install Golang 1.16.
2. Run `make run`

**To run with docker:**
1. Start the docker daemon
2. Run `make docker-build`
3. Run `make docker-run`

**Testing and Linting:**

*Run unit tests with:*
```
make test
```
*lint*:
```
make lint
```

**To push out to a quay.io repo:**
1. docker login with encrypted CLI password from quay.io:
```
docker login -u=<username> --password-stdin < <path_to_encrypted_cli_password> quay.io
```
1. `export IMG="quay.io/<username>/hello-world-service:<version>"`
2. Run `make docker-build`
3. Run `make docker-push`
