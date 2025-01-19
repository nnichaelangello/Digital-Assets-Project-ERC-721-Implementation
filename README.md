# Digital Assets Project: ERC-721 Implementation

## Overview
This project is part of the **Programming Assignment: Digital Assets Project** from the course offered by **The State University of New York**. It involves the implementation of the ERC-721 standard for creating and managing Non-Fungible Tokens (NFTs) on the Ethereum blockchain. The project demonstrates a foundational understanding of blockchain technology, smart contract development, and decentralized asset management.

## Project Title
**"Digital Assets Project: ERC-721 NFT Implementation on Ethereum"**

## Key Features
This project provides a fully functional implementation of the ERC-721 standard with the following features:

- **Minting Tokens**: Create unique NFTs with a specific token ID.
- **Ownership Tracking**: Maintain records of token ownership using the `ownerOf` function.
- **Transfer Functionality**: Allow users to transfer tokens securely with the `transferFrom` function.
- **Approval Mechanism**: Implement `approve` and `setApprovalForAll` for managing third-party access to tokens.
- **Event Emission**: Log events like `Transfer`, `Approval`, and `ApprovalForAll` to provide transparency.

## Smart Contract Details

### Contract Name
`ERC721`

### Standards Implemented
- **ERC-165**: For interface detection.
- **ERC-721**: Core NFT standard for managing non-fungible tokens.

### Functions Included
1. **Minting**
   - `_mint(address to, uint256 id)`
   - `mint(address to)`
2. **Ownership**
   - `ownerOf(uint256 id)`
   - `balanceOf(address owner)`
3. **Transfer**
   - `transferFrom(address from, address to, uint256 id)`
4. **Approval**
   - `approve(address spender, uint256 id)`
   - `setApprovalForAll(address operator, bool approved)`
   - `isApprovedForAll(address owner, address operator)`

### Events
- `Transfer(address indexed from, address indexed to, uint256 indexed id)`
- `Approval(address indexed owner, address indexed spender, uint256 indexed id)`
- `ApprovalForAll(address indexed owner, address indexed operator, bool approved)`

## Deployment Details

- **Deployed Contract Address**: `0xd7C87aD0ff0D9F654B6Af13EDA4B4fe262f17c2a`
- **Development Wallet Address**: `0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d`
- **Beneficiary Wallet Address**: `0x542DFD1C3A027d61B8bCfb3BA104681BA4C3aa07`

## Prerequisites
To interact with the smart contract, you need:

- **Node.js and npm**: For development and testing.
- **Truffle or Hardhat**: To compile, test, and deploy the contract.
- **Metamask Wallet**: For interacting with the blockchain.
- **Ganache**: For local Ethereum blockchain testing.

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/erc721-digital-assets.git
   cd erc721-digital-assets
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Compile the contract:
   ```bash
   npx hardhat compile
   ```

4. Deploy the contract:
   ```bash
   npx hardhat run scripts/deploy.js --network <network_name>
   ```

5. Test the contract:
   ```bash
   npx hardhat test
   ```

## Interaction with the Contract

You can interact with the contract using the following tools:

1. **Web3.js**: Use JavaScript to call contract methods.
2. **Ethers.js**: A lightweight library for Ethereum interaction.
3. **Remix IDE**: Test the contract using a browser-based development environment.
4. **Frontend Integration**: Build a React or Vue.js frontend for user interaction.

## Example Usage

### Minting a Token
```javascript
const tokenId = 1;
await contract.mint("0x542DFD1C3A027d61B8bCfb3BA104681BA4C3aa07", tokenId);
console.log(`Token ID ${tokenId} minted successfully!`);
```

### Transferring a Token
```javascript
const tokenId = 1;
await contract.transferFrom(
  "0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d",
  "0x542DFD1C3A027d61B8bCfb3BA104681BA4C3aa07",
  tokenId
);
console.log(`Token ID ${tokenId} transferred successfully!`);
```

## Challenges and Learnings
- **Gas Optimization**: Efficient state updates and storage.
- **Security**: Validating inputs to prevent vulnerabilities.
- **Interface Compliance**: Ensuring full adherence to ERC-721 and ERC-165 standards.

## Future Improvements
1. **Metadata Integration**: Add support for token metadata (e.g., images, descriptions).
2. **Royalty Support**: Implement EIP-2981 for NFT royalties.
3. **Batch Minting**: Allow multiple tokens to be minted in a single transaction.
4. **Frontend Interface**: Build a user-friendly interface for interaction.

## Resources
- [Ethereum Documentation](https://ethereum.org/en/developers/)
- [ERC-721 Standard](https://eips.ethereum.org/EIPS/eip-721)
- [Solidity Documentation](https://docs.soliditylang.org/)
- [OpenZeppelin Library](https://openzeppelin.com/contracts/)

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

![image](https://github.com/user-attachments/assets/e55cc779-2187-4f6b-94a4-6d2ce00c4545)

Feel free to fork, contribute, and raise issues to improve this project!

