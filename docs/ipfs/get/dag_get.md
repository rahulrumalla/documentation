# dag_get

## /api/v0/dag/get

Get a dag node from ipfs.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/dat/get?arg=<key>`

#### REQUEST PARAMS
1. `arg` _[required]_ - The IPFS object hash

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/dag/get?arg=QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `data`
- `links` - An array of associated link objects

#### BODY
```js
{
    data: "CAISFXZlcnNpb24gMSBvZiBteSB0ZXh0ChgV",
    links: [ ]
}
```