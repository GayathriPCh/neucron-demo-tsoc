# SPV Wallet Workshop - TSSOC'24

This project demonstrates the basic usage of the Neucron SDK, including authentication, wallet management, and transactions.

### Gist used
https://gist.github.com/enlightenedfish/d8a90600638e4e74b3c00e3569b910a4

## Installation

This project uses [Bun](https://bun.sh/) as the runtime environment. Bun is faster than npm for running JavaScript/TypeScript projects.

1. Install Bun (or use npm )

2. Clone the repository and navigate to the project directory:
   ```sh
   git clone https://github.com/your-username/neucron-sdk-project.git
   cd neucron-sdk-project
   ```

3. Install the dependencies:
   ```sh
   bun install
   ```

## Usage

1. Import the Neucron SDK and initialize it:
   ```javascript
   import NeucronSDK from "neucron-sdk";

   const neucron = new NeucronSDK();

   const authModule = neucron.authentication;
   const walletModule = neucron.wallet;
   ```

2. Authentication:

   - Login:
     ```javascript
     const loginResponse = await authModule.login({ email: "your-email", password: "your-password" });
     console.log(loginResponse);
     ```

   - Sign Up (commented out):
     ```javascript
     // const signUpResponse = await authModule.signUp({ email: "your-email", password: "your-password" });
     // console.log(signUpResponse);
     ```

3. Wallet Management:

   - Get Default Wallet Balance:
     ```javascript
     const DefaultWalletBalance = await walletModule.getWalletBalance({});
     console.log(DefaultWalletBalance);
     ```

   - Get Wallet Keys (commented out):
     ```javascript
     // const walletKeys = await walletModule.getWalletKeys({});
     // console.log(walletKeys);
     ```

   - Get Addresses by Wallet ID (commented out):
     ```javascript
     // const addresses = await walletModule.getAddressesByWalletId({});
     // console.log(addresses);
     ```

4. Transactions:

   - Spend Transaction (commented out):
     ```javascript
     // const options = {
     //     outputs: [
     //       {
     //         address: 'rohan@dev.neucron.io',
     //         note: 'gurudakshina',
     //         amount: 10
     //       }
     //     ]
     //   };

     // const payResponse = await neucron.pay.txSpend(options)
     // console.log(payResponse);
     ```

5. Wallet History (commented out):
   ```javascript
   // const walletHistory = await walletModule.getWalletHistory({});
   // console.log(walletHistory);
   ```

6. Wallet Creation and Management (commented out):
   ```javascript
   // console.log('initiating wallet');
   // const walletCreation1 = await walletModule.createWallet({ walletName: 'Hello tsoc1' });
   // console.log(walletCreation1);

   // const walletBalance = await walletModule.getWalletBalance({ walletId: walletCreation1.walletID });
   // console.log(walletBalance);

   // const addresses = await walletModule.getAddressesByWalletId({ walletId: walletCreation1.walletID });
   // console.log(addresses);

   // const mnemonic = await walletModule.getMnemonic({ walletId: walletCreation1.walletID });
   // console.log(mnemonic);

   // const allUtxos = await walletModule.getAllUtxos({ walletId: walletCreation1.walletID });
   // console.log(allUtxos);

   // const xPubKeys = await walletModule.getXPubKeys({ walletId: walletCreation1.walletID });
   // console.log(xPubKeys);
   ```

## Learnings

- Signing up and logging in with Neucron Wallet
- Using paymail ID
- Utilizing Swagger UI for Neucron
- Getting wallet addresses
- Understanding transactions and satoshis

## Running the Project

To run the project, use the following command:
```
npm run workshop.js
```
 if using npm or

 
```
bun run workshop.js
```
 if using bun

