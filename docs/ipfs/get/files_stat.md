# /api/v0/files/stat

Display file status.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/files/stat?arg=<path>&offset=<value>&count=<value>`

#### REQUEST PARAMS
- `arg` _[required]_ - Path to file to be read.
- `format` _[optional]_ - Print statistics in given format.
- `hash` _[optional]_ - Print only hash.
- `size` _[optional]_ - Print only size.

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/files/stat?arg=/ipfs/QmdEikikgbEKw9HNPbxFrPUbs9z8Ux91tbjgDuCLuERnQN"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Hash` - Hash of the object
- `Size` - size of file
- `CumulativeSize` - size of the tree
- `Blocks` - number of linked blocks
- `Type` - node type (file or directory)


#### BODY
```json
{
    Hash: "QmdEikikgbEKw9HNPbxFrPUbs9z8Ux91tbjgDuCLuERnQN",
    Size: 82273,
    CumulativeSize: 82287,
    Blocks: 0,
    Type: "file"
}
```