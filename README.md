Goal

The goal of this project is to create a decentralized To-Do List application using the Aptos blockchain. Users can connect their wallet, add tasks, mark tasks as completed, and interact with their To-Do List in a decentralized manner. The project demonstrates the use of Aptos smart contracts and integration with a React frontend.

Scope

This project involves:
Smart Contract Development: Writing and deploying a Move smart contract to manage a To-Do List on the Aptos blockchain.
Frontend Development: Creating a React application with wallet integration to interact with the smart contract.
Wallet Integration: Using Aptos wallet adapters to connect user wallets and interact with the blockchain.
Testing and Deployment: Compiling, testing, and deploying the smart contract, and setting up the frontend application.

Set Up the Move Project

In the To-Do List project, running aptos move compile and aptos move publish will create a config.yaml file with the following content:
yaml
profiles:
   {{{{ network: Devnet
    private_key: "0x1b622df0ef47923ee27cc9f55c544daeab66e3a324f1b7e81103796ddf286617"
    public_key: "0x737036e542f512f7412e737cc944fd7e98c6e65876bc0824d75271daef6bb186"
    account: 30a7d2ec35f86c759536eba3ad87ab15e552ae3df54335b5032d2c5909d28cbd
    rest_url: "https://fullnode.devnet.aptoslabs.com"
    faucet_url: "https://faucet.devnet.aptoslabs.com"}}}}
    
After this, if you work in a Linux environment, type wsl and then install npm and React. The packages you need to install are @aptos-labs/wallet-adapter-react and @aptos-labs/wallet-adapter-ant-design to integrate with the wallet. In the project directory, navigate to cd client and run npm start. Ensure all necessary packages for wallet integration and React are installed. Additionally, add the Petra wallet extension to Chrome to get the output.

screen shot of frontend
1} frontend 
![Screenshot (273)](https://github.com/user-attachments/assets/6e271b7b-ecea-4ddc-876e-6c0f57386bbd)

2} connected wallet (i already added task )
![Screenshot (274)](https://github.com/user-attachments/assets/ac5f54cf-8914-4a87-9c6b-93d6de050a88)

3} Another task added

![Screenshot (275)](https://github.com/user-attachments/assets/efc51d43-d54e-4ac2-945c-551b62b9059e)

![Screenshot (277)](https://github.com/user-attachments/assets/e2b82814-bd6f-45f8-8da8-44b39b27af90)






