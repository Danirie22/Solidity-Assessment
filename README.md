Project: Create a Token

This Solidity program is for beginner programmer of Solidity. It aims to show how the token works.

Description

This program using basic syntax and functions that for beginners. It uses data types, mapping, functions and conditions.
This contract can help you to get more knowledge about Ethereum and blockchain. 

Executing program

To execute this program you need to use online IDE of Solidity, which is https://remix.ethereum.org/
Once you open the link, you can create a file on the contract folder. The file name must be have ".sol" at the end so that the compiler will read it.
After you created a file you can copy paste this code below.

	// SPDX-License-Identifier: MIT
 
	pragma solidity ^0.8.7;

	contract MyToken {

    // public variables here
    string public tokenName = "Gucci";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint(address _address, uint _value)public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value)public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
        
    }
	}

 To compile this code you click the "Solidity Compiler" at the left side of you screen or in simple way you press "ctrl + s". 
 After you compiled the code, you click the bottom of the "Solidity Compiler" which is the "Deploy and run transactions" and click the deplot orange button.
 At the bottom you see the file name of your code. Then click drop down arrow and you can see the variable that your code have and input you have to fill.
 You can see the example address at the top part of the "Deploy and run transactions". You copy the value of "Account" and past it in the mint or burn.
 After that you add value after the comma in address and click the burn or mint to confirm the value. To check the balance, paste the address in balance and click the balance button 
 to see the total balance. 

 I hope I explain it clear and I hope you learned something about this code. Thank you!!

    

