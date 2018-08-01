# dag_put

## /api/v0/dag/put

Add a dag node to IPFS.

### REQUEST

`POST https://ipfs.infura.io:5001/api/v0/dag/put?format=cbor&input-enc=json&pin=false&hash=<value>`

#### REQUEST PARAMS
- `file` _[Required]_ - The path to a file to be added to IPFS.
- `format` _[Optional]_ - cid format for blocks to be created
- `pin` _[Optional]_ - Pin this object when adding. Default: “true”.
- `input-enc` _[Optional]_ - Format that the input object will be. Default: “json”. 
- `hash` _[Optional]_ - Hash function to use.
 
#### EXAMPLE
Argument 'file' is of file type. This endpoint expects a file in the body of the request as `multipart/form-data`.

```bash
// POST
curl "https://ipfs.infura.io:5001/api/v0/dag/put?format=cbor&input-enc=json&pin=false" \
    -X POST \
    -H "Content-Type: multipart/form-data" \
    -F file=@"/sample-result.json" 
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Cid` - Content ID (see more [here](https://github.com/ipld/cid)) 


#### BODY
```json
{
    "Cid": {
        "/": "zdpuAzaZNBehCV84L76P6Zr5APxN8bbGdqvrqPfvX6XKMBYpK"
    }
}
```