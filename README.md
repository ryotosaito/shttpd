# shttpd
HTTP server by bash

## Usage
Execute `shttpd` on your document root directory.
Specify port by environment `$port` (default: 3000).
```sh
$ port=80 shttpd
```

## Features
- returns
  - html
  - jpeg
  - png
  - (others: return as `application/octet-stream`)
- encoding
  - gzip
