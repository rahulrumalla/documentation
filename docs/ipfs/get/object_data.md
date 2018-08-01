# object_data

## /api/v0/object/data

Output the raw bytes of an IPFS object.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/object/data?arg=<key>`

#### REQUEST PARAMS
1. `arg` _[required]_ - Key of the object to retrieve, in base58-encoded multihash format. 

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/object/data?arg=QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### BODY
```
This endpoint returns a `text/plain` response body.
```