# Union Finance contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Resources

- [Website](https://union.finance/)
- [Docs](https://docs.union.finance/)
- [Twitter](https://twitter.com/unionprotocol)

# On-chain context

```
DEPLOYMENT: Goerli, Optimism Goerli
ERC20: DAI
ERC721: none
ERC777: none
FEE-ON-TRANSFER: none
REBASING TOKENS: none
ADMIN: restricted
EXTERNAL-ADMINS: restricted
```

In case of restricted, by default Sherlock does not consider direct protocol rug pulls as a valid issue unless the protocol clearly describes in detail the conditions for these restrictions. 
For contracts, owners, admins clearly distinguish the ones controlled by protocol vs user controlled. This helps watsons distinguish the risk factor. 
Example: 
* `ContractA.sol` is owned by the protocol. 
* `admin` in `ContractB` is restricted to changing properties in `functionA` and should not be able to liquidate assets or affect user withdrawals in any way. 
* `admin` in `ContractC` is user admin and is restricted to only `functionB`

# Audit scope

```
IAssetManager.sol
IDai.sol
IMarketRegistry.sol	
IUDai.sol		
IUnionToken.sol
Controller.sol
OpOwner.sol
UnionLens.sol
WadRayMath.sol
AaveV3Adapter.sol
AssetManager.sol
PureTokenAdapter.sol
IComptroller.sol	
IInterestRateModel.sol	
IMoneyMarketAdapter.sol	
IUToken.sol		
IUserManager.sol
FixedInterestRateModel.sol	
MarketRegistry.sol		
UDai.sol			
UErc20.sol			
UToken.sol
Comptroller.sol		
OpConnector.sol		
OpUNION.sol		
Whitelistable.sol
UserManager.sol		
UserManagerDAI.sol	
UserManagerERC20.sol	
UserManagerOp.sol
```

# Known issues

https://github.com/sherlock-audit/2022-10-union-finance-judging/issues

# About Union Finance

Union is a member-owned credit protocol built on Ethereum where members can underwrite lines of credit to other member addresses.
Union operates as a DAO and enables any address to accumulate a credit line on-chain in a permission-less, crypto-native way. The protocol itself is not an underwriter of risk, but rather a mechanism to lower the cost of coordinating trust into available credit.

By aggregating lines of credit, Union Members can source capital at a lower cost than any single member could on their own. This enables a virtuous circle of more available credit, lower borrowing costs, and increased lending activity.
