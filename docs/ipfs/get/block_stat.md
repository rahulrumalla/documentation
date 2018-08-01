# block_stat

## /api/v0/block/stat

Print information of a raw IPFS block.

### REQUEST

`POST https://ipfs.infura.io:5001/api/v0/block/stat?arg=<key>`

#### REQUEST PARAMS
1. `arg` _[required]_ - The base58 multihash of an existing block to stat.

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/block/stat?arg=QmfQ5QAjvg4GtA3wg3adpnDJug8ktA1BxurVqBD8rtgVjM"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Key` - The base58 multihash string of the block
- `Size` - An integer representing the size in bytes 

#### BODY
```js
{
    Key: "QmfQ5QAjvg4GtA3wg3adpnDJug8ktA1BxurVqBD8rtgVjM",
    Size: 18
}
```