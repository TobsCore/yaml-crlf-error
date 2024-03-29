# Line ending error in YAML #

On windows systems, the line ending CRLF is not supported by [goccy/go-yaml](https://github.com/goccy/go-yaml) library. This repository demos the issue, by providing a minimal viable demo, that showcases the behavior. The folder `ex` contains examples, which can be used to showcase the issue. The demo application can be called via

```bash
go run . -f ex/demo1.yml
```

The only difference between `demo1.yml` and `demo1-unix.yml` are the line-endings. The `demo2*` files are provided to showcase, that the error does not depend on issues with strings in general.

| File             | Line Ending | String Wrapping    |
|------------------|-------------|--------------------|
| `demo1.yml`      | CRLF        | -                  |
| `demo1-unix.yml` | LF          | ""                 |
| `demo2.yml`      | CRLF        | -                  |
| `demo2-unix.yml` | LF          | ""                 |
