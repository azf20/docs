### Ropsten Testnet

RelayHub: [0xAa3E82b4c4093b4bA13Cb5714382C99ADBf750cA](https://ropsten.etherscan.io/address/0xAa3E82b4c4093b4bA13Cb5714382C99ADBf750cA)

Forwarder: [0xeB230bF62267E94e657b5cbE74bdcea78EB3a5AB](https://ropsten.etherscan.io/address/0xeB230bF62267E94e657b5cbE74bdcea78EB3a5AB)

VersionRegistry: [0x9e59Ea5333cD4f402dAc320a04fafA023fe3810D](https://ropsten.etherscan.io/address/0x9e59Ea5333cD4f402dAc320a04fafA023fe3810D)

Accept-Everything Paymaster: [0x05319d82fa69EA8434A967CdF4A2699Db4Ff40e8](https://ropsten.etherscan.io/address/0x05319d82fa69EA8434A967CdF4A2699Db4Ff40e8)

#### Recommeneded Server configuration
gsn-relay-config.json:
```json
{
  "baseRelayFee": 0,
  "pctRelayFee": 70,
  "versionRegistryAddress": "0x9e59Ea5333cD4f402dAc320a04fafA023fe3810D",
  "ownerAddress": "<OWNER_ADDRESS>",
  "gasPriceFactor": 1,
  "confirmationsNeeded": 1,
  "registrationBlockRate": 500000,
  "ethereumNodeUrl": "<NODE_URL>>"
}
```
#### Recommeneded client configuration
```js
  // add the following fields to your GSNConfig:
  const gsnConfig: Partial<GSNConfig> = {
    relayLookupWindowBlocks: 6e5,
    relayRegistrationLookupBlocks: 6e5,
    pastEventsQueryMaxPageSize: Number.MAX_SAFE_INTEGER,
  }
  const gsnProvider = RelayProvider.newProvider({provider: web3Provider, config: gsnConfig})
  await gsnProvider.init()
```
