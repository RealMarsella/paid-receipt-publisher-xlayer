# Deployments

Date: 2026-05-22

## X Layer Testnet (chain ID 1952)

| Item | Value |
|---|---|
| Network | X Layer Testnet (Terigon) |
| Chain ID | `1952` |
| RPC | `https://testrpc.xlayer.tech/terigon` |
| Explorer | `https://www.okx.com/web3/explorer/xlayer-test` |
| Deployer | `0xBc25F65EC030f2A889556c92d2A2D91612Dd1F66` |

### Deployed Contracts

| Contract | Address | Tx Hash |
|---|---|---|
| `ReceiptRegistry` | `0xc4202d5bBd28665961110924798E78BA7Ba68458` | `0x9040024e82be441c7e6dd3382f1afdb67a76d81e1628c20d6f95305287bf1e73` |

### Verification

`eth_getCode` returned 4,368 bytes for `ReceiptRegistry`. Contract is live and queryable via the explorer above.

## Reproduce Deployment

```bash
export XLAYER_RPC_URL=https://testrpc.xlayer.tech/terigon
export DEPLOYER_PRIVATE_KEY=<funded testnet private key>

forge create \
  --rpc-url "$XLAYER_RPC_URL" \
  --private-key "$DEPLOYER_PRIVATE_KEY" \
  --broadcast \
  contracts/src/ReceiptRegistry.sol:ReceiptRegistry
```

Forge script alternative (also works):

```bash
forge script contracts/script/DeployReceiptRegistry.s.sol \
  --rpc-url "$XLAYER_RPC_URL" \
  --broadcast
```

## X Layer Mainnet

Status: not attempted. Hackathon submission is testnet-only.
