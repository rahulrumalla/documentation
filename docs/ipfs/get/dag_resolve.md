# /api/v0/dag/resolve

Resolve ipld block

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/dat/resolve?arg=<key>`

#### REQUEST PARAMS
1. `arg` _[required]_ - The IPFS object hash; the path to resolve

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/dag/resolve?arg=QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Cid` - Content ID (see more [here](https://github.com/ipld/cid)) 
- `RemPath`

#### BODY
```js
{
    Cid: {
        /: "QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy"
    },
    RemPath: ""
}
```