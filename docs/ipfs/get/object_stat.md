# object_stat

## /api/v0/object/stat

Get stats for the DAG node named by key.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/object/stat?arg=<key>`

#### REQUEST PARAMS
- `arg` _[required]_ - Key of the object to retrieve, in base58-encoded multihash format. 

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/object/stat?arg=QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Hash` - Hash of the object
- `NumLinks` - number of links the node contains
- `BlockSize` - size of the raw serialized node
- `LinksSize` - size of the links block section
- `DataSize` - size of data block section
- `CumulativeSize` - size of the tree (BlockSize + link sizes)

#### BODY
```json
{
    Hash: "QmZtmD2qt6fJot32nabSP3CUjicnypEBz7bHVDhPQt9aAy",
    NumLinks: 0,
    BlockSize: 29,
    LinksSize: 2,
    DataSize: 27,
    CumulativeSize: 29
}
```