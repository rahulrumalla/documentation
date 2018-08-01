# files_write

## /api/v0/files/write

Write to a mutable file in a given filesystem.

### REQUEST

`POST https://ipfs.infura.io:5001/api/v0/files/write?format=cbor&input-enc=json&pin=false&hash=<value>`

#### REQUEST PARAMS
- `file` _[Required]_ - The file to be added to IPFS.
- `path` _[Required]_ - The path to write the file to.
- `offset` _[Optional]_ - Byte offset to begin writing at.
- `create` _[Optional]_ - Create the file if it does not exist.
- `truncate` _[Optional]_ - Truncate the file to size zero before writing. 
- `count` _[Optional]_ - Maximum number of bytes to read.
 
#### EXAMPLE
Argument 'file' is of file type. This endpoint expects a file in the body of the request as `multipart/form-data`.

```bash
// POST
curl "https://ipfs.infura.io:5001/api/v0/files/write?arg=/ipfs-file-test?create=true" \
    -X POST \
    -H "Content-Type: multipart/form-data" \
    -F file="/readme.txt" 
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