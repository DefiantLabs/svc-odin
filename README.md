# svc-odin

IBC Paths maintained by Defiant Labs. If you want to participate in these paths feel free to use the CONFIGs below.

## Wallets

- [axelar14vrutp488vh4y2n07atq3r6d578zgwr434uyjg](https://www.mintscan.io/odin/axelar/axelar14vrutp488vh4y2n07atq3r6d578zgwr434uyjg)
- [odin14vrutp488vh4y2n07atq3r6d578zgwr43mv04r](https://mainnet.odinprotocol.io/accounts/odin14vrutp488vh4y2n07atq3r6d578zgwr43mv04r)
- [osmo14vrutp488vh4y2n07atq3r6d578zgwr4aqeu0m](https://www.mintscan.io/osmosis/account/osmo14vrutp488vh4y2n07atq3r6d578zgwr4aqeu0m)

## Axelar

[client Open](https://www.mintscan.io/axelar/txs/E7ED2A81E7F11BAC16A6FB4E212A96FF5371CD57DA2C8E2F9DEAFFCF5F3BB107?height=7460395)  
[connection open](https://www.mintscan.io/axelar/txs/231BE1FC5AB9556A24C24902F6B8FBA3D8133EE6BAA5B981CA767796F5298391?height=7460403)  
[channel open](https://www.mintscan.io/axelar/txs/29641FBA3927072C135E899058D13A769B80CD81DA574E02CD45CE4F126C3982?height=7460410)
[ibc test](https://www.mintscan.io/axelar/txs/C2BE7208CE8007EF3BD1B7827B8CE05F5CB4E73B2A82CE9D5B228D27001E9F0F?height=7460597)

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
  axelar:
    type: cosmos
    value:
      key: default
      chain-id: axelar-dojo-1
      rpc-addr: https://rpc.axelar.strange.love:443
      account-prefix: axelar
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.007uaxl
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      signing-algorithm: ""
      broadcast-mode: batch
      min-loop-duration: 0s
      feegrants: null
  odin:
    type: cosmos
    value:
      key: default
      chain-id: odin-mainnet-freya
      rpc-addr: http://34.79.179.216:26657
      # rpc-addr: https://odin-rpc.lavenderfive.com:443
      # rpc-addr: https://odin-mainnet-rpc.autostake.com:443
      account-prefix: odin
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.0125loki
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      signing-algorithm: ""
      broadcast-mode: batch
      min-loop-duration: 0s
      feegrants: null
paths:
  mainnet-odin-axelar:
    src:
      chain-id: odin-mainnet-freya
      client-id: 07-tendermint-66
      connection-id: connection-51
    dst:
      chain-id: axelar-dojo-1
      client-id: 07-tendermint-150
      connection-id: connection-135
    src-channel-filter:
      rule: "allowlist"
      channel-list: ["channel-37"]
```

## Osmosis

### GO RELAYER CONFIG

```
global:
  api-listen-addr: :5183
  timeout: 10s
  memo: "defiantlabs"
  light-cache-size: 20
chains:
  odin:
    type: cosmos
    value:
      key: default
      chain-id: odin-mainnet-freya
      rpc-addr: http://34.79.179.216:26657
      account-prefix: odin
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.0125loki
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      signing-algorithm: ""
      broadcast-mode: batch
      min-loop-duration: 0s
      feegrants: null
  osmosis:
    type: cosmos
    value:
      key: default
      chain-id: osmosis-1
      rpc-addr: https://rpc.osmosis.strange.love:443
      account-prefix: osmo
      keyring-backend: test
      gas-adjustment: 1.2
      gas-prices: 0.0025uosmo
      min-gas-amount: 0
      debug: false
      timeout: 20s
      block-timeout: ""
      output-format: json
      sign-mode: direct
      extra-codecs: []
      coin-type: 118
      signing-algorithm: ""
      broadcast-mode: batch
      min-loop-duration: 0s
      feegrants: null
paths:
  mainnet-odin-osmosis:
    src:
      chain-id: odin-mainnet-freya
      client-id: 07-tendermint-10
      connection-id: connection-9
    dst:
      chain-id: osmosis-1
      client-id: 07-tendermint-2007
      connection-id: connection-1551
    src-channel-filter:
      rule: "allowlist"
      channel-list: ["channel-3"]
```
