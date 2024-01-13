## Blockchain

The Blockchain class has two private properties, networkID and blockchainID.
When instantiating the class it will convert the constructor properties to Buffers and store them on the private properties networkID and blockchainID

**EXAMPLES**

```typescript
const someInstance = new Blockchain(
  12345,
  "1234567890987654321234567890987654321234567898765432123456789098"
);
```

## constructor(networkId, blockchainId)

constructor takes two parameters `networkID` and `blockchainID` and then it converts it to buffer and stores it to the class private properties

**PARAMETERS**

- `networkID`: number - network id of type number
- `blockchainID`: string - blockchainID of type string

## blockchain.fetch(method, url, data)

The fetch method makes an axios request to the provided url with the provided method and data and returns Promise<AxiosResponse>.

**PARAMETERS**

- `method`: Method - axios method type. Eg: 'get', 'post'
- `url`: string - the url to be called
- `data`: object - params for the url

**RETURNS**

Promise<AxiosResponse>

## blockchain.toBuffer()

The toBuffer method joins the private properties and returns it.

**RETURNS**

Buffer

## blockchain.fromBuffer(bytes, offset)

The fromBuffer method reads from the input parameter, bytes, at the offset and populates the instance of the Blockchain's respective networkID and blockchainID properties.

**PARAMETERS**

- `bytes`: Buffer - bytes of type Buffer
- `offset`: number - offset of type number

**RETURNS**

number
