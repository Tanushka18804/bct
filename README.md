# bct Step 1: Open Remix IDE

Go to 👉 https://remix.ethereum.org

This is an online Solidity compiler and IDE.

Create a new workspace or use the default one.

In the “contracts” folder, create a new file named Bank.sol.

Step 2: Write the Solidity Code

In Bank.sol, write the following smart contract:
Step 3: Compile the Contract

1. Click on the Solidity Compiler tab (⚙️ icon on left sidebar).


2. Select compiler version 0.8.8 (as written in the pragma line).


3. Click Compile Bank.sol.


4. Make sure no errors appear.




---

Step 4: Deploy on a Test Network

1. Open the Deploy & Run Transactions tab (Ethereum icon 💠).


2. In “Environment”, select Injected Provider - MetaMask.

It will connect Remix with your MetaMask wallet.



3. Ensure your MetaMask is connected to a test network like Sepolia or Goerli and has some test ETH (you can get from a faucet).


4. Click Deploy — MetaMask will ask for confirmation. Approve the transaction.




---

Step 5: Interact with the Contract

After deployment, under Deployed Contracts, you’ll see your Bank contract.

Click the dropdown arrow ⬇️ to expand it.

You will see buttons for:

deposit

withdraw

showBalance

accOwner

balance



Try calling them:

Deposit any number (e.g. 100) → click deposit.

Then click showBalance → it should return 100.

Withdraw 50 → click withdraw.

Click showBalance again → it should now show 50.


⚠️ Common Issue — “showBalance not working”

If the “showBalance” button doesn’t show output:

Ensure it’s marked as view and returns a value.

Code should be:

function showBalance() public view returns (uint256) {
    return balance;
}

Also, after deploying, click the blue button beside showBalance (not orange, because it’s a view function).
Step 6: Verify & Save

Check your transactions in MetaMask under Activity.

Optionally, copy the contract address and verify it on https://sepolia.etherscan.io (if deployed on Sepolia).
