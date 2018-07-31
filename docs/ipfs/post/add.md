# /api/v0/add

Add a file or directory to ipfs.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/add?recursive=false&quiet=<value>&quieter=<value>&silent=<value>&progress=<value>&trickle=<value>&only-hash=<value>&wrap-with-directory=<value>&hidden=<value>&chunker=<value>&pin=true&raw-leaves=<value>&nocopy=<value>&fscache=<value>&cid-version=0&hash=sha2-256`

#### REQUEST PARAMS
- `file` _[Required]_ - The path to a file to be added to ipfs.
- `recursive` _[Optional]_ - Add directory paths recursively. Default: “false”.
- `quiet` _[Optional]_ - Write minimal output.
- `quieter` _[Optional]_ - Write only final hash.
- `silent` _[Optional]_ - Write no output.
- `progress` _[Optional]_ - Stream progress data.
- `trickle` _[Optional]_ - Use trickle-dag format for dag `generation`.
- `only-hash` _[Optional]_ - Only chunk and hash - do not write to disk.
wrap-with-directory _[Optional]_ - Wrap files with a directory object.
- `hidden` _[Optional]_ - Include files that are hidden. Only takes effect on recursive add.
chunker [string]: Chunking algorithm to use.
- `pin` _[Optional]_ - Pin this object when adding. Default: “true”.
- `raw-leaves` _[Optional]_ - Use raw blocks for leaf nodes. (experimental).
- `nocopy` _[Optional]_ - Add the file using filestore. (experimental).
- `fscache` _[Optional]_ - Check the filestore for pre-existing blocks. (experimental).
- `cid-version` [int]: Cid version. Non-zero value will change default of ‘raw-leaves’ to true. (experimental). Default: “0”.
- `hash` [string]: Hash function to use. Will set Cid version to 1 if used. (experimental). Default: “sha2-256”.

 
#### EXAMPLE
Argument 'file' is of file type. This endpoint expects a file in the body of the request as `multipart/form-data`.

```bash
// POST
curl "https://ipfs.infura.io:5001/api/v0/add?pin=false" \
    -X POST \
    -H "Content-Type: multipart/form-data" \
    -F file="/sample-result.json" 
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Name` - Name of the object
- `Hash` - Hash  of the uploaded object
- `Size` - integer indication size in bytes


#### BODY
```json
{
    "Name": "sample-result.json",
    "Hash": "QmSTkR1kkqMuGEeBS49dxVJjgHRMH6cUYa7D3tcHDQ3ea3",
    "Size": "2120"
}
```