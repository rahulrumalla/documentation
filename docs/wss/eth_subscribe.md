# eth_subscribe

Creates a new subscription over particular events. The node will return a subscription id. For each event that matches the subscription a notification with relevant data is send together with the subscription id.

### REQUEST PARAMS
- `SUBSCRIPTION TYPE NAME` _[required]_ 
    - `newHeads`- Subscribing to this, fires a notification each time a new header is appended to the chain, including chain reorganizations. Users can use the bloom filter to determine if the block contains logs that are interested to them.
    - `logs` - Returns logs that are included in new imported blocks and match the given filter criteria. In case of a chain reorganization previous sent logs that are on the old chain will be resend with the removed property set to true. Logs from transactions that ended up in the new chain are emitted. Therefore a subscription can emit logs for the same transaction multiple times.
        - `address` - either an address or an array of addresses. Only logs that are created from these addresses are returned (optional)
        - `topics` - only logs which match the specified topics (optional)
    - `syncing` - Indicates when the node starts or stops synchronizing. The result can either be a boolean indicating that the synchronization has started (true), finished (false) or an object with various progress indicators.
    - `newPendingTransactions` - Returns the hash for all transactions that are added to the pending state and are signed with a key that is available in the node. When a transaction that was previously part of the canonical chain isn't part of the new canonical chain after a reogranization its again emitted.
- `OPTIONAL ARGUMENTS` 
    - `includeTransactions` - A flag indicating to whether include transactions in the response 

#### EXAMPLE
```bash
>wscat -c wss://mainnet.infura.io/ws 

// newHeads
>{"id": 1, "method": "eth_subscribe", "params": ["newHeads", {"includeTransactions": true}]}

// logs
>{"id": 1, "method": "eth_subscribe", "params": ["logs", {"address": "0x8320fe7702b96808f7bbc0d4a888ed1468216cfd", "topics": ["0xd78a0cb8bb633d06981248b816e7bd33c2a35a6089241d099fa519e361cab902"]}]}

// newPendingTransactions
>{"id": 1, "method": "eth_subscribe", "params": ["newPendingTransactions"]}

// syncing
>{"id": 1, "method": "eth_subscribe", "params": ["syncing"]}
```

### RESPONSE

#### RESULT FIELDS
- `SUBSCRIPTION ID` - ID of the newly created subscription on the node

#### BODY

```json
{
    "id": 1, 
    "jsonrpc": "2.0", 
    "result": "0x9cef478923ff08bf67fde6c64013158d"
}
```
