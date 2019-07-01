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
  - css
  - javascript
  - plain text
  - jpeg
  - png
  - (others: return as `application/octet-stream`)
- encoding
  - gzip (requires `gzip` command)
  - deflate (requires `pigz` command)
- security
  - return 403 against path traversal

## Requirements
- bash ^4.x
- GNU sed (`sed` or `gsed`)
