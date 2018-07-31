# /api/v0/pin/add

Pin objects to local storage.

### REQUEST

`POST curl "https://ipfs.infura.io:5001/api/v0/pin/add?arg=<ipfs-path>&recursive=true&progress=<value>"`

#### REQUEST PARAMS
- `arg` _[Required]_ - Path to object(s) to be pinned.
- `recursive` _[Optional]_ - Recursively pin the object linked to by the specified object(s). Default: “true”
- `progress` _[Optional]_ - Show progress. 

#### EXAMPLE
Argument 'file' is of file type. This endpoint expects a file in the body of the request as `multipart/form-data`.

```bash
// POST
curl "https://ipfs.infura.io:5001/api/v0/pin/add?arg=/ipfs/QmSTkR1kkqMuGEeBS49dxVJjgHRMH6cUYa7D3tcHDQ3ea3" 
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Pins` - An array of Pin hashes


#### BODY
```json
{
    "Pins": [
        "QmSTkR1kkqMuGEeBS49dxVJjgHRMH6cUYa7D3tcHDQ3ea3"
    ],
}
```