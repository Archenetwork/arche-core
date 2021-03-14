# ArcheFi Core Contract
## introduction
The Project ArcheFi provides a convenient OPTION platform. An Option Ticket may be created by ANY address ANONYMOUSLY. The tickets are established by ArcheFI's contract-factory as an independent contract.Interactions With Option Contract are decentralized (except statistical Data of Created Options).   

## Functions/Interfaces
Here are 2 Contracts,Main-Contract and Factory-Contract.
### Main Contract

| Function Name | Brief Introduction |
| --- | --- |
|Set_ERC20_Gen_Lib(address lib)   | Set Address of ERC20 Generator Lib (DEPLOYMENT ONLY) |
|Set_Trading_Charge_Lib(address lib) | Set Address of Charging Lib (DEPLOYMENT ONLY) |
|Set_System_Reward_Address(address addr) |Set Address of ERC20 Token For Option Reward  (DEPLOYMENT ONLY)|
|Set_Factory_Lib(address addr) | Set Address of Factory contract (DEPLOYMENT ONLY) |
|Create(address token_head,address token_tail)  | Create an Option Ticket from Factory Contract |
    
### Factory-Contract

| Function Name | Brief Introduction |
| --- | --- |
| Set_DSwap_Main_Address(address addr)   | Set Address of EMain Contract (DEPLOYMENT ONLY) |
| Set_Initializing_Params(uint256 total_amount_head ,uint256 total_amount_tail ,uint256 limit_head ,uint256 limit_tail ,address rival_head,address rival_tail , uint256 pair_dlo ,uint256 option_dlo)| Option Creator Set parameters of Option |
| Claim_For_Head() | Address claim for the option (HEAD side)|
| Claim_For_Tail() | Address claim for the option (TAIL side)|
| Deposit_For_Head(uint256 amount) | Address pay remaining ERC20 of the option  (HEAD side)|
| Deposit_For_Tail(uint256 amount) | Address pay remaining ERC20 of the option  (TAIL side)|
| Withdraw_Head() | Get ERC20 Tokens when option closed or not matched (HEAD side) |
| Withdraw_Tail() | Get ERC20 Tokens when option closed or not matched (TAIL side) |
