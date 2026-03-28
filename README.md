# Lottery.sol
Base - Smart Contract Deployed by Remix Lottery.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Lottery {
    address[] public players;

    function enter() public payable {
        require(msg.value > 0.01 ether, "Minimum 0.01 ETH");
        players.push(msg.sender);
    }

    function getPlayers() public view returns (address[] memory) {
        return players;
    }
}
