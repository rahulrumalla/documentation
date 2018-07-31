# /api/v0/files/read

Read a file in a given MFS (mutable file system).

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/files/read?arg=<path>&offset=<value>&count=<value>`

#### REQUEST PARAMS
- `arg` _[required]_ - Path to file to be read.
- `offset` _[optional]_ - Byte offset to begin reading from.
- `count` _[optional]_ - Maximum number of bytes to read.

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/files/read?arg=/ipfs/QmdEikikgbEKw9HNPbxFrPUbs9z8Ux91tbjgDuCLuERnQN"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:


#### BODY
```
This endpoint returns a `text/plain` response body.
```