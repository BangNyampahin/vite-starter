
![tw-banner](https://github.com/thirdweb-example/vite-starter/assets/57885104/cfe2164b-b50b-4d8e-aaaa-31331da2d647)

# vite-starter

Starter template to build onchain applications with [thirdweb](https://thirdweb.com) and [vite](https://vitejs.dev/). 

## Features 

- thirdweb & vite pre-installed and configured to reduce setup steps
- ConnectButton to onboard users to your application

## Installation

Install the template using [thirdweb create](https://portal.thirdweb.com/cli/create)

npx thirdweb install
ConnectButton } from "thirdweb/react";
import thirdwebIcon from "./thirdweb.svg";
import { client } from "./client";

export function App() {
	return (
		<main className="p-4 pb-10 min-h-[100vh] flex items-center justify-center container max-w-screen-lg mx-auto">
			<div className="py-20">
				<Header />

				<div className="flex justify-center mb-20">
					<ConnectButton
						client={client}
						appMetadata={{
							name: "Example app",
							url: "https://example.com",
						}}
					/>
				</div>

				<ThirdwebResources />
			</div>
		</main>
	);
}

function Header() {
	return (
		<header className="flex flex-col items-center mb-20 md:mb-20">
			<img
				src={thirdwebIcon}
				alt=""
				className="size-[150px] md:size-[150px]"
				style={{
					filter: "drop-shadow(0px 0px 24px #a726a9a8)",
				}}
			/>

			<h1 className="text-2xl md:text-6xl font-bold tracking-tighter mb-6 text-zinc-100">
				thirdweb SDK
				<span className="text-zinc-300 inline-block mx-1"> + </span>
				<span className="inline-block -skew-x-6 text-violet-500"> vite </span>
			</h1>

			<p className="text-zinc-300 text-base">
				Read the{" "}
				<code className="bg-zinc-800 text-zinc-300 px-2 rounded py-1 text-sm mx-1">
					README.md
				</code>{" "}
				file to get started.
			</p>
		</header>
	);
}

function ThirdwebResources() {
	return (
		<div className="grid gap-4 lg:grid-cols-3 justify-center">
			<ArticleCard
				title="thirdweb SDK Docs"
				href="https://portal.thirdweb.com/typescript/v5"
				description="thirdweb TypeScript SDK documentation"
			/>

			<ArticleCard
				title="Components and Hooks"
				href="https://portal.thirdweb.com/typescript/v5/react"
				description="Learn about the thirdweb React components and hooks in thirdweb SDK"
			/>

			<ArticleCard
				title="thirdweb Dashboard"
				href="https://thirdweb.com/dashboard"
				description="Deploy, configure, and manage your smart contracts from the dashboard."
			/>
		</div>
	);
}

function ArticleCard(props: {
	title: string;
	href: string;
	description: string;
}) {
	return (
		<a
			href={`${props.href}?utm_source=vite-template`}
			target="_blank"
			className="flex flex-col border border-zinc-800 p-4 rounded-lg hover:bg-zinc-900 transition-colors hover:border-zinc-700"
			rel="noreferrer"
		>
			<article>
				<h2 className="text-lg font-semibold mb-2">{props.title}</h2>
				<p className="text-sm text-zinc-400">{props.description}</p>
			</article>
		</a>
	);
}



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
