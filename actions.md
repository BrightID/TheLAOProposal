# LAO BrightID Proposed Actions

## Whitelist Subs tokens
BrightID Subscriptions (“Subs”) tokens ([etherscan address](https://etherscan.io/token/0x61CEAc48136d6782DBD83c09f51E23514D12470a)) will be added to the whitelist of tokens that can be held by The LAO.

## Investment Proposal
The LAO will purchase 50,000 BrightID Subs from the [sponsorship dashboard](https://sp.brightid.org). Subs are a discounted stream of [sponsorships](https://medium.com/brightid/brightid-sponsorships-5327a8d39f1e) that can be resold to businesses that need BrightID.

### BBIZ DAO Agent to purchase Subs
Because The LAO in its current version lacks agent capabilities, it will use BrightID's administrative DAO (BBIZ DAO) to make the purchase.

#### Grant
The LAO will grant 50,000 DAI to BrightID's administrative DAO (BBIZ DAO) at its [Aragon agent address](https://mainnet.aragon.org/#/brightidbiz/organization): `0x7ea598f29812673975334c1445ae5c9158b66cb8`.

#### Purchase Subs
BBIZ DAO's agent will interact with the sponsorship dashboard to buy 50,000 Subs.

#### Returning Subs as tribute
BBIZ DAO's agent will create a proposal to tribute 50,000 Subs to The LAO. No shares or other tokens will be granted to BBIZ DAO in return.

## ERC-20 `Transfer` and `TransferFrom` compliance
In order to comply with the “token whitelisting” section in the [article on The LAO smart contracts](https://medium.com/@thelaoofficial/the-lao-joins-forces-with-moloch-dao-and-metacartel-to-begin-to-standardize-dao-related-smart-b6ee4b0db071), [BrightID Main DAO](https://mainnet.aragon.org/#/brightid/organization/) has renounced its [pauser role](https://github.com/BrightID/Sponsorship-Subscriptions-SmartContracts/blob/master/node_modules/openzeppelin-solidity/contracts/access/roles/PauserRole.sol) from the subscriptions token as can be seen from the [smart contract’s event logs](https://etherscan.io/address/0x61CEAc48136d6782DBD83c09f51E23514D12470a#events). (Filter by `0xcd265ebaf09df2871cc7bd4133404a235ba12eff2041bb89d9c714a2621c7c7e` for `PauserRemoved` events and `0x6719d08c1888103bea251a4ed56406bd0c3e69723c8a1686e017e7bbe159b6f8` for `PauserAdded` events.)

By removing all pauser roles, BrightID Main DAO has removed all possible interference with the `transfer` and `transferFrom` functions of the Subs token as defined in the [ERC-20 standard](https://eips.ethereum.org/EIPS/eip-20) and [implemented by open-zepplin](https://github.com/BrightID/Sponsorship-Subscriptions-SmartContracts/blob/master/node_modules/openzeppelin-solidity/contracts/token/ERC20/ERC20.sol). The makes the Subs token safe for use by The LAO's smart contract.
