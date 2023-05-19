# svc-odin

IBC Paths created and maintained by Defiant Labs.  If you want to participate in these paths feel free to use the CONFIGs below.

## Wallets

- [axelar14vrutp488vh4y2n07atq3r6d578zgwr434uyjg](https://www.mintscan.io/odin/axelar/axelar14vrutp488vh4y2n07atq3r6d578zgwr434uyjg)
- [odin14vrutp488vh4y2n07atq3r6d578zgwr43mv04r](https://mainnet.odinprotocol.io/accounts/odin14vrutp488vh4y2n07atq3r6d578zgwr43mv04r)
- [osmo14vrutp488vh4y2n07atq3r6d578zgwr4aqeu0m](https://www.mintscan.io/osmosis/account/osmo14vrutp488vh4y2n07atq3r6d578zgwr4aqeu0m)


## Axelar

[client Open]()  
[connection open]()  
[channel open]()

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
    dst:
      chain-id: axelar-dojo-1
    src-channel-filter:
      rule: ""
      channel-list: []
```

## Osmosis

[client Open]()  
[connection open]()  
[channel open]()

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
    dst:
      chain-id: osmosis-1
    src-channel-filter:
      rule: ""
      channel-list: []
```