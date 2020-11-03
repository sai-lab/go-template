# go-template

![Unit Test](https://github.com/sai-lab/go-template/workflows/Unit%20Test/badge.svg)
![Lint](https://github.com/sai-lab/go-template/workflows/Lint/badge.svg)
![Go](https://img.shields.io/github/go-mod/go-version/sai-lab/go-template)
[![PkgGoDev](https://pkg.go.dev/badge/github.com/sai-lab/go-template)](https://pkg.go.dev/github.com/sai-lab/go-template)


This repository is template repository for golang developper in Saisho labo.

## Getting Started

First, push `use this template` button in this repository.
Next rename variables for your application.
Here's the startup script.

```bash
(
    export APPLICATION=your-application-name
    export USER=your-user-name
    export REPOSITORY=$USER/$APPLICATION
    grep -l 'hello' Dockerfile .github/workflows/*.yaml | xargs sed -i.bak -e "s/hello/$APPLICATION/g"
    grep -l 'sai-lab/go-template' * | xargs sed -i.bak -e "s@sai-lab/go-template@$REPOSITORY@g"
)
```

### Docker Build in local

```bash
docker build -t ghcr.io/your-user-name/your-application-name .
docker run ghcr.io/your-user-name/your-application-name
```

## CI

- Lint (`go vet`, `golangci-lint`)
- Unit Tests
- Publish library documents
- Build and push container image to `ghcr.io`
- Vulnerability scanning in container image

## Documentation

GoDoc is generated by GitHub actions when your application released.

## License

Put your application license.
