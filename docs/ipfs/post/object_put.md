# object_put

## /api/v0/object/put

Store input as a DAG object, print its key.

### REQUEST

`POST http://ipfs.infura:5001/api/v0/object/put?inputenc=json&datafieldenc=text&pin=false`

#### REQUEST PARAMS
- `file` _[Required]_ - the file to be stored as a DAG object.
- `inputenc` _[Optional]_ - Encoding type of input data. One of: {“protobuf”, “json”}. Default: “json”. 
- `datafieldenc` _[Optional]_ - Encoding type of the data field, either “text” or “base64”. Default: “text”.
- `pin` _[Optional]_ - Pin this object when adding. Default: “false”.
 
#### EXAMPLE
Argument 'file' is of file type. This endpoint expects a file in the body of the request as `multipart/form-data`.

```bash
// POST
curl "https://ipfs.infura.io:5001/api/v0/object/put?inputenc=json&datafieldenc=text&pin=false" \
    -X POST \
    -H "Content-Type: multipart/form-data" \
    -F file="node.json" 
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Hash` - Hash of the object


#### BODY
```json
{
    "Hash": "QmZZmY4KCu9r3e7M2Pcn46Fc5qbn6NpzaAGaYb22kbfTqm"
}
```