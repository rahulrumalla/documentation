# /api/v0/files/mkdir

Make directories on a MFS (Mutable File System).

### REQUEST

`POST https://ipfs.infura.io:5001/api/v0/files/mkdir?arg=<path>`

#### REQUEST PARAMS
- `arg` _[Required]_ - Path to dir to make.
 
#### EXAMPLE

```bash
// POST
 curl "https://ipfs.infura.io:5001/api/v0/files/mkdir?arg=/ipfs-examples-dir"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### BODY
```
This endpoint returns a `text/plain` response body.
```