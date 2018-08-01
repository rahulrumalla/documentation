# block_put

## /api/v0/block/put

Store input as an IPFS block.

### REQUEST

`POST https://ipfs.infura.io::5001/api/v0/block/put?format=v0&mhtype=sha2-256&mhlen=-1`

#### REQUEST PARAMS
- `file` _[Required]_ - The path to a file to be added to IPFS.
- `format` _[Optional]_ - cid format for blocks to be created with. Default: “v0”. 
- `mhtype` _[Optional]_ - multihash hash function. Default: “sha2-256”.
- `mhlen` _[Optional]_ - multihash hash length. Default: “-1”. 
 
#### EXAMPLE
Argument 'file' is of file type. This endpoint expects a file in the body of the request as `multipart/form-data`.

```bash
// POST
curl "https://ipfs.infura.io:5001/api/v0/block/put" \
    -X POST \
    -H "Content-Type: multipart/form-data" \
    -F file="/purpink.jpeg" 
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Key` - Key of the block
- `Size` - integer indication size in bytes


#### BODY
```json
{
    "Key": "QmaYL7E4gDTPNfLxrCEEEcNJgcHBJ55NxxTnxpDKWqMtJ3",
    "Size": 2392
}
```