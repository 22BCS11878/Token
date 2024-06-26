
# EVM PROJECT
This project shows how to use Solidity, the main programming language for Ethereum smart contracts, to build a bespoke coin on the blockchain. The repository contains deployment scripts, the Solidity source code, and detailed instructions for configuring and deploying your own token.

# DESCRIPTION
This project is an in-depth guide to creating a custom token on the Ethereum blockchain using Solidity. It covers the entire process from writing the Solidity code to deploying the token on the Ethereum network. The project aims to provide a clear understanding of the fundamental concepts of smart contracts and token creation, making it easier for developers to create their own tokens for various applications such as Initial Coin Offerings (ICOs), decentralized applications (dApps), and other blockchain-based projects.

# GETTING STARTED
Executing program To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at
https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.18+commit.87f61d96.js

Click the "+" symbol in the left-hand sidebar to start a new file once you are on the Remix website. Save the file (MyToken.sol, for example) with the.sol extension. The code below should be copied and pasted into the file:
contract MyToken {
   
    // public variables here
    string public tokenname= "Dezire";
    string public tokenabbrv = "BMW";
    uint public totalsupply = 0;

    // mapping variable here
    mapping(address=>uint)public balances;


    // mint function
    function mint(address _address,uint _values)public{
    totalsupply+=_values;
    balances[_address]+=_values;
    }

    // burn function
    function burn (address _address,uint _values)public{
    if(balances[_address]>_values){
     totalsupply-=_values;
     balances[_address]-=_values;
      }
   }
}
 Select the "Solidity Compiler" tab from the sidebar on the left to begin compiling the code. Click "Compile MyToken.sol" after ensuring that the "Compiler" option is selected to "0.8.4" (or another compatible version).

Selecting the "Deploy & Run Transactions" tab from the left-hand sidebar will allow you to deploy the contract after the code has been compiled. Click the "Deploy" button after choosing the "MyToken" contract from the dropdown menu.

After the contract is deployed, you can call functions like balanceOf and transfer using Remix's deployed contract interface.

# Authors
Vishavjeet Singh

# License
This project is licensed under the MIT License - see the LICENSE.md file for details
