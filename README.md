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
#### *BURN* - This function burns  tokens by taking the address and value of tokens to be burned as the arguments and decreases the  value of TotalSupply variable and  address balance if the amount to be burned is lesser or equal to the amount in the balance of the address.

## **GETTING STARTED**
### **EXECUTING PROGRAM**
#### To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
#### Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here
   
   
   string public token_name = "Firespiko";
   string public token_abbrv = "FSP";
   uint public  TotalSupply = 0;
   
    // mapping variable here
   
   mapping(address => uint) public balances;
   
    // mint function
   
   function mint(address _address,uint _value) public {
      TotalSupply += _value;
      balances[_address] += _value;
   }
    // burn function
   
   function burn(address _address,uint _value) public {
      if (balances[_address] >= _value){
         TotalSupply -= _value;
         balances[_address] -= _value;
      }     
   }
```
#### To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18+" (or another compatible version), and then click on the "Compile MyToken.sol" button.
#### Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.
#### Once the contract is deployed click on three variables to check their values and in the account section choose any address  and click copy to clipboard.Click on the drop down on mint function and click on the address parameter and paste the address and enter the number of tokens to  mint in the value parameter.Click the mint function.Click on the TotalSupply  variable and balances mapping by pasting address to check whether if the transaction is complete.
#### Now the same process is done for the burn unction to burn the token(i.e to decrease the no of tokens) and the transaction will not go through if the no of tokens is greater to burn is greater than the no of tokens in address.

### **AUTHORS**
#### **Firespiko**

### **LISCENCE**
#### This project is licensed under the MIT License - see the LICENSE.md file for details
