

# Web3.py Simple Storage

After working on Remix to start my start contract and solidity development journey, I understood the limitations of using an IDE.

In order for me to deploy test and automate everything about my smart contract development cycle I decided to connect my Solidity work with a more 
traditional programming language like Python by working with the web3.py package.



## Key Learnings

1. Limitations of Remix (hard integration with other parts of a project/doesn't have Python)

2. Working with web3.py

3. Submit a transaction that deploys the contract on a local ganache chain (https://www.trufflesuite.com/ganache)

4. Submit a transaction that deploys the contract on a testnet (Rinkeby) (via a RINKEBY_RPC_URL= https://infura.io/)

5. Ability to retrieve my contract on EtherScan - Rinkeby Testnet Network - 0xF40E321C58166b4Af9a778bc3B640b7F7A1a309a - most exciting part :


![Screen Shot 2022-03-28 at 11 24 35](https://user-images.githubusercontent.com/68856635/160357427-7037f32d-d2ab-473f-95cf-847e613b4e1a.png)

![Screen Shot 2022-03-28 at 11 25 17](https://user-images.githubusercontent.com/68856635/160357467-934ab9db-a220-4f0f-a252-c6bfceb53c85.png)


# Steps to reproduce 

1. Clone this repo

```
git clone https://github.com/Rubenadhoute/Simple_storage_web3.git
cd web3_py_simple_storage
```

2. Setup a [local ganache chain](https://www.trufflesuite.com/ganache)
3. Install requirements

```bash
pip install -r requirements.txt
```

4. Set your private keys and address, and adjust this section appropriately:

```python
# For connecting to ganache
w3 = Web3(Web3.HTTPProvider("http://0.0.0.0:8545"))
chaind_id = 1337
my_address = "0x94B806BB0e455576ea46193D9DBbB08d1cc57Da9"
private_key = os.getenv("PRIVATE_KEY")
```

5. Set your private key as an environment variable by running `export PRIVATE_KEY=0xasdfasdfasfdasf` and run `python deploy.py`



To run on a testnet, just change these variables to whatever testnet you want to work with:

```
w3 = Web3(Web3.HTTPProvider("http://0.0.0.0:8545"))
chaind_id = 1337
my_address = "0x94B806BB0e455576ea46193D9DBbB08d1cc57Da9"
private_key = os.getenv("PRIVATE_KEY")
```

And make sure you have testnet ETH for whatever testnet you're on!

## License

This project is licensed under the [MIT license](LICENSE).
