# files_flush

## /api/v0/files/flush

Flush a given path’s data to disk.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/files/flush?arg=<path>`

#### REQUEST PARAMS
- `arg` _[required]_ - Path to file to be read.

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/files/flush?arg=/ipfs-docs-example"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### BODY
```
This endpoint returns a `text/plain` response body.
```