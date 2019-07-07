# shttpd
HTTP server by bash

## Usage
Execute `shttpd` on your document root directory.
For use on network, call from `ncat` (from nmap. not `nc`).
```sh
$ shttpd
$ ncat -kl -c shttpd localhost 3000 #open port 3000, keep port alive(-k)
$ ncat --ssl -kl -c 'SCHEME=https shttpd' localhost 3000 #run as https server
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
- cgi
  - executes `.cgi` file (`+x` flag required)
- security
  - returns 403 against path traversal

## Requirements
- bash ^4.3
- nkf

## IMPORTANT NOTICE
DO NOT USE shttpd ON YOUR PRODUCTION (OR INSECURE) ENVIRONMENT  
WE DO NOT TAKE ANY RESPONSIBILITIES
