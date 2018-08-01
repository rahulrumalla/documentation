# /api/v0/get

Download IPFS objects.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/get?arg=<ipfs-path>&output=<value>&archive=false&compress=false&compression-level=-1`

#### REQUEST PARAMS
- `arg` _[required]_ - The IPFS object hash
- `output` _[optional]_ - The path where the output should be stored. 
- `archive` _[optional]_ - Output a TAR archive. Default: “false”. 
- `compress` _[optional]_ - Compress the output with GZIP compression. Default is “false”. 
- `compression-level` _[optional]_ - The level of compression (1-9). Default: “-1”. 
 
#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/get?arg=QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy&archive=true"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:


#### BODY
```
This endpoint returns a `text/plain` response body.
```