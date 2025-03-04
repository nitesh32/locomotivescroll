## Sources



[website](https://docs.sui.io/references/cli/cheatsheet)
[website](https://docs.sui.io/guides/developer/first-app/client-tssdk)
[website](https://docs.sui.io/references/sui-graphql)


To use Sui in TypeScript, you will need to install the `@mysten/sui` package. Here's a step-by-step guide:

1. **Install the package**: You can install the `@mysten/sui` package using your preferred package manager. The documentation recommends using `pnpm` or `yarn`. 
   ```bash
$ pnpm add @mysten/sui
```
   or
   ```bash
$ yarn add @mysten/sui
```

2. **Import the package**: Once installed, you can import the package in your TypeScript file.
   ```typescript
import { SuiClient } from '@mysten/sui';
```

3. **Create a Sui client instance**: To interact with the Sui network, you need to create a `SuiClient` instance. You can do this by calling the `new SuiClient()` constructor and passing the URL of the Sui fullnode you want to connect to.
   ```typescript
const suiClient = new SuiClient('https://fullnode.devnet.sui.io');
```

4. **Use the Sui client**: With the `SuiClient` instance, you can now use its methods to interact with the Sui network. For example, you can use the `getObjectsOwnedByAddress` method to get the objects owned by a specific address.
   ```typescript
const address = '0xyour_address';
const objects = await suiClient.getObjectsOwnedByAddress(address);
console.log(objects);
```

For more information, you can refer to the [Sui TypeScript SDK documentation](https://sdk.mystenlabs.com/typescript).

Here is a code block that demonstrates the basic usage:
```typescript
import { SuiClient } from '@mysten/sui';

// Create a new Sui client instance
const suiClient = new SuiClient('https://fullnode.devnet.sui.io');

// Get the objects owned by a specific address
const address = '0xyour_address';
const objects = await suiClient.getObjectsOwnedByAddress(address);
console.log(objects);
```
Note: Replace `'0xyour_address'` with the actual address you want to query.

Please let me know if you have any further questions or need more assistance. 

Also, can you please confirm if you have any specific use case in mind for using Sui in TypeScript, so I can provide more tailored guidance?
