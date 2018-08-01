# id

## /api/v0/id

Show IPFS node id info.

### REQUEST

`GET https://ipfs.infura.io:5001/api/v0/get?arg=<peerid>&format=<value>`

#### REQUEST PARAMS
- `arg` _[optional]_ - Peer ID of node to look up.
- `format` _[optional]_ - Optional output format

 
#### EXAMPLE
```bash
// GET
curl "https://ipfs.infura.io:5001/api/v0/id?arg=Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N"
```

### RESPONSE

On success, the call to this endpoint will return with 200 and the following body:

#### RESULT FIELDS
- `ID` - Peer ID hash
- `PublicKey` - Public Key of the node
- `Addresses` - Listen addresses of the Host
- `AgentVersion` - Client version
- `ProtocolVersion` - holds the current protocol version for a client running this code

#### BODY
```json
{
    ID: "Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N",
    PublicKey: "CAASpgIwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCq1Rc1+JFY1Ds4dHHPs/sshcC/8Oh5dG/kkIK/HmUpib2/kRg242O1hIGDb2yKDN9TFa43TZDYYNNGJbHRRr8Y1J5bBX6jHHGW0i85NEZm74LbU023vVjYUMoOjT7QPnjSUym7zB2vOIydQSLmSSSta2lZi4hPhH+fDzJoL2cQ241i2o6Ay/AoorayJO9vMj3N4ptjrW2aWhLdQZA+Lg6mtpu0GdpnoYJQvki/T40ZCgOvB/9gG/Z1guUvhXzl3DS8TbPrSqUMWe97oyN0J1VLnVw2UKGOW+hyNhJ9oLG0MesRTIa2p9OOKAB55Taf7cBY9tSKzCNDxfi5NP8PEyJNAgMBAAE=",
    Addresses: [
        "/ip4/127.0.0.1/tcp/4001/ipfs/Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N",
        "/ip4/10.0.21.194/tcp/4001/ipfs/Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N",
        "/ip4/172.17.0.1/tcp/4001/ipfs/Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N",
        "/ip6/::1/tcp/4001/ipfs/Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N",
        "/ip4/18.232.150.108/tcp/4001/ipfs/Qmdnso85PCsvwSPp9NDZHqfoK872onaw2rgckgJSkWdK5N"
    ],
    AgentVersion: "go-ipfs/0.4.14/",
    ProtocolVersion: "ipfs/0.1.0"
}
```