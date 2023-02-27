
# Surge contest details

Borrow, lend, long or short any token on any chain.

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Resources

- [Surge Protocol Overview]([url](https://medium.com/surge-fi/introduction-to-surge-protocol-overview-34cc828d7c50))

# On-chain context

The README is a **very important** document for the audit. Please fill it out thoroughly and include any other specific info that security experts will need in order to effectively review the codebase.

**Some pointers for filling out the section below:**  
ERC20/ERC721/ERC777/FEE-ON-TRANSFER/REBASING TOKENS:  
*Which tokens do you expect will interact with the smart contracts? Please note that these answers have a significant impact on the issues that will be submitted by Watsons. Please list specific tokens (ETH, USDC, DAI) where possible, otherwise "Any"/"None" type answers are acceptable as well.*

ADMIN:
*Admin/owner of the protocol/contracts.
Label as TRUSTED, If you **don't** want to receive issues about the admin of the contract being able to steal funds. 
If you want to receive issues about the Admin of the contract being able to steal funds, label as RESTRICTED & list specific acceptable/unacceptable actions for the admins.*

EXTERNAL ADMIN:
*These are admins of the protocols your contracts integrate with (if any). 
If you **don't** want to receive issues about this Admin being able to steal funds or result in loss of funds, label as TRUSTED
If you want to receive issues about this admin being able to steal or result in loss of funds, label as RESTRICTED.*
 
```
DEPLOYMENT: Mainnet, Optimism, Arbitrum, Fantom, Avalanche, Polygon, BNB Chain and other EVM chains
ERC20: any non-rebasing
ERC721: none
ERC777: none
FEE-ON-TRANSFER: none
REBASING TOKENS: none
ADMIN: restricted
EXTERNAL-ADMINS: restricted
```


Please answer the following questions to provide more context: 
### Q: Are there any additional protocol roles? If yes, please explain in detail:
1) The roles
2) The actions those roles can take 
3) Outcomes that are expected from those roles 
4) Specific actions/outcomes NOT intended to be possible for those roles

A: There is a single fee operator role. It can only set the fee on interest (up to 20% fee) and the fee recipient address. Unexpected loss of funds due to the operator role should be considered high severity bugs.

___
### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
A: Pool contracts (aka receipt tokens) should be compliant with the ERC20 token standard.

___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
A: Loan and collateral contracts are considered by the Pool contracts as trusted, ERC20-compliant and non-rebasing token contracts. It's the users' responsibility to choose pools with valid non-malicious token contracts. This include re-entrancy risk due to external calls to these 2 contracts.

____
### Q: Please provide links to previous audits (if any).
A: None available

___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)? 
A: No.
_____

### Q: In case of external protocol integrations, are the risks of an external protocol pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality. 
A: NOT ACCEPTABLE


# Audit scope


[surge-protocol-v1 @ b7cb1dc2a2dcb4bf22c765a4222d7520843187c6](https://github.com/Surge-fi/surge-protocol-v1/tree/b7cb1dc2a2dcb4bf22c765a4222d7520843187c6)
- [surge-protocol-v1/src/Factory.sol](surge-protocol-v1/src/Factory.sol)
- [surge-protocol-v1/src/Pool.sol](surge-protocol-v1/src/Pool.sol)


[List of all contracts in scope]

# About Surge

Surge is a hyperstructure lending protocol that allows anyone to deployer their own lending pool. It utilizes a novel mechanism called Algorithmic Collateral Ratios in order to eliminate the need for price oracles in DeFi lending.
