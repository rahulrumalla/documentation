# files_cp

## /api/v0/files/cp

Copy files to a MFS (Mutable File System).

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/files/cp?arg=<source>&arg=<dest>`

#### REQUEST PARAMS
- `arg` _[Required]_ - Source object to copy. ( the ipfs/[hash] link )
- `arg` _[Required]_ - Destination to copy object to. ( on the MFS )
 
#### EXAMPLE

```bash
// GET
 curl "https://ipfs.infura.io:5001/api/v0/files/cp?arg=/ipfs/QmSTkR1kkqMuGEeBS49dxVJjgHRMH6cUYa7D3tcHDQ3ea3&arg=/ipfs-examples-docs-001"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### BODY
```
This endpoint returns a `text/plain` response body.
```