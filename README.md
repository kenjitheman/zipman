## Archive compressor/extractor in golang

###

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original.svg" height="200" alt="go logo"  />
</div>

###

## Supported formats and functionality:

- `zip` (compression/extraction/adding)
- `tar` (compression/extraction/adding)
- `tar.gz` (compression/extraction/adding)
- `7z` (compression/extraction)
- `bz2` (compression/extraction)
- `rar` (extraction)

## Project structure:

```go
├── 7z.go
├── bzip2.go
├── go.mod
├── go.sum
├── LICENSE
├── rar.go
├── README.md
├── tar.go
├── targz.go
└── zip.go
```

## Installation

```shell
go get github.com/kenjitheman/zipman
```

## Usage

```go
package main

import "github.com/kenjitheman/zipman"

func main() {
	zipman.CompressToZip("./file.zip", []string{"./man.txt", "./hello.txt"})

    // zipman.AddFileToZip(zipWriter *zip.Writer, filename string)
	// zipman.ExtractZip("./file.zip", "./man")
}
```

```rust
➜  zipman git:(master) ✗ go run main.go
[SUCCESS] Zip compression completed successfully for file: ./file.zip
```

## Contributing

- Pull requests are welcome, for major changes, please open an issue first to
  discuss what you would like to change.

## License

- [MIT](https://choosealicense.com/licenses/mit/)
