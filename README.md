
![tw-banner](https://github.com/thirdweb-example/vite-starter/assets/57885104/cfe2164b-b50b-4d8e-aaaa-31331da2d647)

# vite-starter

Starter template to build onchain applications with [thirdweb](https://thirdweb.com) and [vite](https://vitejs.dev/). 

## Features 

- thirdweb & vite pre-installed and configured to reduce setup steps
- ConnectButton to onboard users to your application

## Installation

Install the template using [thirdweb create](https://portal.thirdweb.com/cli/create)

npx thirdweb install



```bash
  npx thirdweb create app --vite
```
forge install https://github.com/thirdweb-dev/contracts

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@thirdweb-dev/contracts/base/ERC721Base.sol";

contract MyNFT is ERC721Base {
    constructor(
        address _defaultAdmin,
        string memory _name,
        string memory _symbol,
        address _royaltyRecipient,
        uint128 _royaltyBps
    ) ERC721Base(_defaultAdmin, _name, _symbol, _royaltyRecipient, _royaltyBps) {}
}
npm i thirdweb
import {
  createThirdwebClient,
  getContract,
} from "thirdweb";
import { defineChain } from "thirdweb/chains";

// create the client with your clientId, or secretKey if in a server environment
const client = createThirdwebClient({
  clientId: "2509b4189ca0092f9113adc3c7996ae1",
});

// connect to your contract
const contract = getContract({
  client,
  chain: defineChain(8453),
  address: "0x8B5EED3184Ba83BCb2627df60d974aAC94e81a56",
});
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@thirdweb-dev/contracts/base/ERC721Base.sol";

contract MyNFT is ERC721Base {
    constructor(
        address _defaultAdmin,
        string memory _name,
        string memory _symbol,
        address _royaltyRecipient,
        uint128 _royaltyBps
    ) ERC721Base(_defaultAdmin, _name, _symbol, _royaltyRecipient, _royaltyBps) {}
}
[/Script/Thirdweb.ThirdwebRuntimeSettings]
ClientID=
BundleID=


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file:

`2509b4189ca0092f9113adc3c7996ae1`

To learn how to create a client ID, refer to the [client documentation](https://portal.thirdweb.com/typescript/v5/client). 

## Run locally

Install dependencies

```bash
yarn
```

Start development server

```bash
yarn dev
```

Create a production build

```bash
yarn build
```

Preview the production build

```bash
yarn preview
```

## Additional Resources

- [Documentation](https://portal.thirdweb.com/typescript/v5)
- [Templates](https://thirdweb.com/templates)
- [YouTube](https://www.youtube.com/c/thirdweb)
- [Blog](https://blog.thirdweb.com)

## Need help?

For help or feedback, please [visit our support site](https://thirdweb.com/support)
