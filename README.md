#  **MY TOKEN**

#### This Solidity program is a Token creation program that performs simple tasks such as minting and burning tokens.The purpose of the program is to learn how a simple token can be created in solidity.

## **DESCRIPTION**

#### This program is a simple contract written in solidity with three state variables,1 mapping and two functions.
### **Variables** 
#### This program has three variables named token_name,token_abbrv and TotalSupply which stores token name, token abbreviation and total supply respectively.
### **Mapping** 
#### This program cointains a mapping named balances which maps address to their respective balances.
### **Functions**
#### This program contains two functions named mint and burn which does the following operations -

#### *MINT* - This function mints new tokens by taking the address and value of tokens to be minted as the arguments and increases the  value of TotalSupply variable and  address balance.
#### *BURN* - This function burns  tokens by taking the address and value of tokens to be burned as the arguments and decreases the  value of TotalSupply variable and  address balance if the amount to be burned is lesser or equa to the amount in the balance of the address.
