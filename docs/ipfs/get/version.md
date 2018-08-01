# version

## /api/v0/version

Show ipfs version information.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/get?number=false&commit=false&repo=false&all=false`

#### REQUEST PARAMS
- `number` _[optional]_ - Only show the version number. Default is false
- `commit` _[optional]_ - Show the commit hash. Default is false
- `repo` _[optional]_ - Show repo version. Default is false
- `all` _[optional]_ - Show all version information. Default is false

 
#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/version?arg=Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `Version` - Current version number
- `Commit` - Current commit id
- `Repo` - Version number of the repo
- `System` - System information
- `Golang` - GoLang runtime version

#### BODY
```json
{
    Version: "0.4.14",
    Commit: "",
    Repo: "6",
    System: "amd64/linux",
    Golang: "go1.10"
}
```