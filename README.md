
# [project name] contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Resources

- [[resource1]](url)
- [[resource2]](url)

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
DEPLOYMENT: [e.g. mainnet, Arbitrum, Optimism, ..]
ERC20: [e.g. any, none, USDC, USDC and USDT]
ERC721: [e.g. any, none, UNI-V3]
ERC777: [e.g. any, none, {token name}]
FEE-ON-TRANSFER: [e.g. any, none, {token name}]
REBASING TOKENS: [e.g. any, none, {token name}]
ADMIN: [trusted, restricted, n/a]
EXTERNAL-ADMINS: [trusted, restricted, n/a]
```


Please answer the following questions to provide more context: 
### Q: Are there any additional protocol roles? If yes, please explain in detail:
1) The roles
2) The actions those roles can take 
3) Outcomes that are expected from those roles 
4) Specific actions/outcomes NOT intended to be possible for those roles

A: 

___
### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
A:

___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
A: 

____
### Q: Please provide links to previous audits (if any).
A:

___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)? 
A: 
_____

### Q: In case of external protocol integrations, are the risks of an external protocol pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality. 
A: [ACCEPTABLE/NOT ACCEPTABLE] 


# Audit scope


[surge-protocol-v1 @ b7cb1dc2a2dcb4bf22c765a4222d7520843187c6](https://github.com/Surge-fi/surge-protocol-v1/tree/b7cb1dc2a2dcb4bf22c765a4222d7520843187c6)
- [surge-protocol-v1/src/Factory.sol](surge-protocol-v1/src/Factory.sol)
- [surge-protocol-v1/src/Pool.sol](surge-protocol-v1/src/Pool.sol)


[List of all contracts in scope]

# About [project name]
