# create move dir and go inside (Preparing for smart contract)
1. Initialize move config -> aptos move init --name my_todo_list
output:
{
  "Result": "Success"
}

2. Run this command to setup devnet (It will create .aptos folder with yaml file) -> aptos init --network devnet
output: 
Configuring for profile default
Configuring for network Devnet
Enter your private key as a hex literal (0x...) [Current: None | No input: Generate new key (or keep one if present)]

No key given, generating key...
Account 0xfd34.... doesn't exist, creating it and funding it with 100000000 Octas
Account 0xfd34.... funded successfully

---
Aptos CLI is now set up for account 0xfd34.... as profile default!  Run `aptos --help` for more information about commands
{
  "Result": "Success"
}

## Imporant: If wanna use your existing wallet address add private key of wallet address

3. add fund in account - aptos account fund-with-faucet --account default
output:
{
  "Result": "Added 100000000 Octas to account 0xfd34...."
}

## Imporant: If wanna use your existing wallet address, in place of default, use your wallet public key

4. now update Move.toml with created config , 
-> update todolist_addr with address showing on above Result - 0xfd34....
-> add, addr='fd34....', where fd34.... is in config.yml account key's value

5. update Source code with move code

6. Compile & Test -> aptos move compile
Output based on code -
Compiling, may take a little while to download git dependencies...
UPDATING GIT DEPENDENCY https://github.com/aptos-labs/aptos-core.git
INCLUDING DEPENDENCY AptosFramework
INCLUDING DEPENDENCY AptosStdlib
INCLUDING DEPENDENCY MoveStdlib
BUILDING my_todo_list
{
  "Result": [
    "7ef02....::todolist"
  ]
}

7. Write test function using #[test]

8. Publish Smart Contract in Aptos Chain -> aptos move publish
Compiling, may take a little while to download git dependencies...
UPDATING GIT DEPENDENCY https://github.com/aptos-labs/aptos-core.git
INCLUDING DEPENDENCY AptosFramework
INCLUDING DEPENDENCY AptosStdlib
INCLUDING DEPENDENCY MoveStdlib
BUILDING my_todo_list
package size 3040 bytes
Do you want to submit a transaction for a range of [211900 - 317800] Octas at a gas unit price of 100 Octas? [yes/no] >
yes
{
  "Result": {
    "transaction_hash": "0xc59fe....",
    "gas_used": 2119,
    "gas_unit_price": 100,
    "sender": "fd34....",
    "sequence_number": 0,
    "success": true,
    "timestamp_us": 1712801455608986,
    "version": 666787,
    "vm_status": "Executed successfully"
  }
}

# in Recat app - client folder
1. create recat app and change required ui, This code using ant ui, so install -> npm i antd@5.1.4
Note: updated App.tsx and index.tsx

2. install wallet adapter library for aptos 
-> npm i @aptos-labs/wallet-adapter-react
-> npm i @aptos-labs/wallet-adapter-ant-design

3. install wallet (wallet adapter support: https://github.com/aptos-labs/aptos-wallet-adapter#supported-wallet-packages)
-> Here example for petra wallet  (https://petra.app/)- npm i petra-plugin-wallet-adapter


4. To read aptos chan data install ts sdk - npm i @aptos-labs/ts-sdk

5. Run npm start and test"# APTOS-project_TO-DO-LIST" 
