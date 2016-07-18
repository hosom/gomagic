# magic
golang libmagic bindings

## Installation

```
sudo apt-get install libmagic-dev

go get github.com/hosom/magic
```

## Usage

Bindings are 1:1 mappings of the C library, so if you're familiar with libmagic's C interface, then you should be set. This feels a little bit unnattural in Go, but it keeps the implementation simple and easy to support in the long run. 

### Initialize a libmagic instance

```go
m, err := magic.Open(magic.MAGIC_NONE)
if err != nil {
  log.Fatal(err)
}
```

### Check a file

```go
result, err := m.File("/path/to/file")
if err != nil {
  log.Fatal(err)
}
fmt.Println(result)
```
