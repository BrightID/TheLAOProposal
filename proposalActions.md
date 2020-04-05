# LAO BrightID Proposal Actions

## Whitelist Subs tokens
At the initial launch of The LAO, the BrightID subscriptions (“Subs”) token ([etherscan address](https://etherscan.io/token/0x61CEAc48136d6782DBD83c09f51E23514D12470a)) will be whitelisted.

### ERC-20 `Transfer` and `TransferFrom` compliance
In order to comply with the “token whitelisting” section in the [article on The LAO smart contracts](https://medium.com/@thelaoofficial/the-lao-joins-forces-with-moloch-dao-and-metacartel-to-begin-to-standardize-dao-related-smart-b6ee4b0db071), [BrightID Main DAO](https://mainnet.aragon.org/#/brightid/organization/) has renounced its [pauser role](https://github.com/BrightID/Sponsorship-Subscriptions-SmartContracts/blob/master/node_modules/openzeppelin-solidity/contracts/access/roles/PauserRole.sol) from the subscriptions token as can be seen from the [smart contract’s event logs](https://etherscan.io/address/0x61CEAc48136d6782DBD83c09f51E23514D12470a#events). (Filter by `0xcd265ebaf09df2871cc7bd4133404a235ba12eff2041bb89d9c714a2621c7c7e` for `PauserRemoved` events and `0x6719d08c1888103bea251a4ed56406bd0c3e69723c8a1686e017e7bbe159b6f8` for `PauserAdded` events.)

By removing all pauser roles, BrightID Main DAO has removed all possible interference with the `transfer` and `transferFrom` functions of the Subs token as defined in the [ERC-20 standard](https://eips.ethereum.org/EIPS/eip-20) and [implemented by open-zepplin](https://github.com/BrightID/Sponsorship-Subscriptions-SmartContracts/blob/master/node_modules/openzeppelin-solidity/contracts/token/ERC20/ERC20.sol). The makes the Subs token safe for use by The LAO's smart contract.

## Investment Proposal

### BBIZ DAO Agent to purchase subs

### Returning Subs as tribute
