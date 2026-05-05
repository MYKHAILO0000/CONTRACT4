// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract BaseNFT is ERC721 {
    uint256 public nextTokenId;
    constructor() ERC721("BaseNFT", "BNFT") {}
    function mint() external {
        _safeMint(msg.sender, nextTokenId);
        nextTokenId++;20
    }
}

