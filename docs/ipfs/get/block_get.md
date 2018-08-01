# block_get

## /api/v0/block/get

Get a raw IPFS block.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/block/get?arg=<key>`

#### REQUEST PARAMS
- `arg` _[required]_ - The base58 multihash of an existing block to get.

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/block/get?arg=QmaYL7E4gDTPNfLxrCEEEcNJgcHBJ55NxxTnxpDKWqMtJ3"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### BODY
```
This endpoint returns a `text/plain` response body.
```