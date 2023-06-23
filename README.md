
# Solidity Beginner Assessment
This Solidity program is a mint and burn program where we provide some basic required variables in to get the resultant total supply after the successful execution of the program. The main idea is to get hands-on experience in working with the Solidity programming language. 


## Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.
The contract has public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply), a mapping of addresses to balances, a mint function that increases the total supply and the balance of the address by that amount, and a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and the address's balance. Lastly, the burn function should have conditionals to make sure the balance of the account is greater than or equal to the amount that is supposed to be burned.
## Getting Started
## 1. Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT

pragma solidity 0.8.18;

/*
       REQUIREMENTS
  1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
 2. Your contract will have a mapping of addresses to balances (address => uint)
3. You will have a mint function with two parameters: an address and a value. 
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
   
    
    string public token_Name="Assessment";
   
    string public token_Abbreviation="Ass";

    uint public total_Supply=0;


    // mapping variable here

    mapping(address => uint) public balances;
   

    // mint function

   function mint(address _address, uint _value) public {

    balances[_address]+=_value;

   total_Supply+= _value;
     }
   

   // burn function

   function burn(address _address, uint _value) public {

    if(balances[_address]>=_value)

     {

     balances[_address] -= _value;

      total_Supply -=  _value;

    }

    }
 
  }




To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, then click the "Deploy" button.

Once the contract is deployed, you can interact with it by following the below mentioned steps:

1 Pasting the  same account address in mint address, burn address, and balance address.

2 Input the mint value and click on transact.

3. Input the burn value and click on transact.

4. At last check the total supply after the complete execution of the program.

For example:

mint value: 2000

burn value: 1000

final total supply: 2000-1000=1000



## Author
Sehajpreet Kaur
## License
This project is licensed under the MIT License - see the LICENSE.md file for details.
