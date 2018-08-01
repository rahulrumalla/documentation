# files_stat

## /api/v0/files/stat

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
curl "https://ipfs.infura.io:5001/api/v0/files/stat?arg=/ipfs-docs-example"
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
    Hash: "QmVMvdPwiXvdSTKhDrTpQaW1zjoX5g9w72PWHsnSSTz2F2",
    Size: 29,
    CumulativeSize: 87,
    Blocks: 1,
    Type: "file"
}
```