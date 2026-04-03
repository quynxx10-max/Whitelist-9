# Whitelist-9
Whitelist.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Whitelist {
    mapping(address => bool) public allowed;

    function addToWhitelist(address _addr) public {
        allowed[_addr] = true;
    }

    function isAllowed(address _addr) public view returns (bool) {
        return allowed[_addr];
    }
}
