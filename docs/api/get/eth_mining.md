# eth_mining

## /v1/jsonrpc/:network/eth_mining

Returns true if client is actively mining new blocks.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_mining`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
// HTTP GET
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_mining

// HTTP POST
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_mining","params": [],"id":1}'
    
// SOCKETS
>wscat -c wss://mainnet.infura.io/ws 
>{"jsonrpc":"2.0","method":"eth_mining","params": [],"id":1}
```

### RESPONSE

#### RESULT FIELDS
- `IS MINING FLAG` - a boolean indicating if the client is mining

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: true
}
```
