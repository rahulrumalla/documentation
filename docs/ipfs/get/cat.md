# cat

## /api/v0/cat

Show IPFS object data.

### REQUEST

`POST https://ipfs.infura.io:5001/api/v0/cat?arg=<key>`

#### REQUEST PARAMS
1. `arg` _[required]_ - The IPFS object hash

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/cat?arg=QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### BODY
```
This endpoint returns a `text/plain` response body.
```