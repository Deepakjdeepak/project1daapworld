# project1daapworld
Retrieve the value of secret_flag from the contract
the code is:

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
