
# Solidity Beginner Assessment
This program basically focuses on creating our own token and performing basic tasks such as minting and burning the amount using the Solidity programming language with the help of the Remix online compiler. 


## Code Logic
1. This program is a simple contract written in Solidity.
2. It has public variables that store the details about your coin.
3. A mapping of addresses to balances.
4. Mint function performs the addition of the total supply and the balance of the address with that amount.
5. Burn function will destroy tokens. It will then subtract the value from the total supply and the address's balance.
6. Lastly, the burn function has an if statement to make sure the balance of the account is greater than or equal to the amount that is supposed to be burned.

## Execution of the program
After opening the Remix website create a new file using the .sol extension and write the following code.

// SPDX-License-Identifier: MIT

pragma solidity 0.8.18;

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



## Code Functionality
To compile the code, click on the "Solidity Compiler" tab and then click on the "Compile SolidityFinalAssesment.sol" button.

After compiling, deploy the contract by clicking on the "Deploy & Run Transactions" tab. Select the "MyToken" contract from the menu, then click the "Deploy" button.

Once the contract is deployed, you can interact with it by following the below-mentioned steps:

1 Pasting the  same account address in mint address, burn address, and balance address.

2 Input the mint value and click on transact.

3. Input the burn value and click on transact.

4. At last check the total supply after the complete execution of the program.

## Author
Sehajpreet Kaur
(21BCS4518@cuchd.in)
## License
This project is licensed under the MIT License - see the LICENSE.md file for details.
