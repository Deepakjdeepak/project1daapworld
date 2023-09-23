# project1daapworld
Retrieve the value of secret_flag from the contract
the code is:

method1;
const Web3 = require('web3');
const web3 = new Web3('YOUR_ETHEREUM_NODE_URL'); // Replace with your Ethereum node URL

const contractAddress = 'YOUR_CONTRACT_ADDRESS'; // Replace with the actual contract address
const contractAbi = [...]; // Replace with the ABI of your contract

const contract = new web3.eth.Contract(contractAbi, contractAddress);

async function getSecretFlag() {
  try {
    const secretFlag = await contract.methods.secret_flag().call();
    console.log(`The secret flag is: ${secretFlag}`);
  } catch (error) {
    console.error('Error:', error);
  }
}

getSecretFlag();

method 2;
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract PrivateFlag {
    string public name = "Anon";
    string private Address = "Private";
    uint8 public age = 13;
    address public wallet = 0x0000000000000000000000000000000000001337;
    uint48 private favourite_number = 1337;
    bytes32[4] private Hashes;
    uint16 public num1 = 1;
    uint16 private num2 = 2;
    bool private Pwn = false;
    bool private pwn = false;
    bool private pwN = false;
    string private secret_flag = "YourSecretFlagValue"; // Replace with the actual secret flag.
    address public owner;

    // Constructor to set the owner of the contract
    constructor() {
        owner = msg.sender;
    }

    // Function to retrieve the secret flag
    function getSecretFlag() public view returns (string memory) {
        return secret_flag;
    }
}
