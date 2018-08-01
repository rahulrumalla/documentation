# object_get

## /api/v0/object/get

Get and serialize the DAG node named by key.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/object/get?arg=<key>`

#### REQUEST PARAMS
- `arg` _[required]_ - Key of the object to retrieve, in base58-encoded multihash format. 

#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/object/get?arg=QmfQ5QAjvg4GtA3wg3adpnDJug8ktA1BxurVqBD8rtgVjM"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `links` - An array of associated link objects
- `data`

#### BODY
```
{
    Links: [ ],
    Data: "version 1 of my text "
}
```