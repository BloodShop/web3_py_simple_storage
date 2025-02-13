> NOTE: This repo has been updated to use the goerli testnet over rinkeby and kovan.

1. Clone this repo

```
git clone https://github.com/BloodShop/web3_py_simple_storage.git
cd web3_py_simple_storage
```

2. Make sure to install following packages || peckage managers

```
pip install web3
pip install python-dotenv
pip install py-solc-x
npm install --global yarn
yarn global add ganache-cli
```

3. Setup a [local ganache chain](https://www.trufflesuite.com/ganache)
4. Install requirements

```bash
pip install -r requirements.txt
```

5. Set your private keys and address, and adjust this section appropriately:

```python
# For connecting to ganache
w3 = Web3(Web3.HTTPProvider("http://127.0.0.1:8545" || "https://sepolia.infura.io/v3/API_KEY_PROJECT"))
chaind_id = 11155111
my_address = "0x6aABE487828603b6f0a3E1C7DAcF7F42bA42A9B2"
private_key = os.getenv("PRIVATE_KEY")
```

To set your private key as an environment variable, run `export PRIVATE_KEY=0xasdfasdfasfdasf`. If you're confused on how environment variables work, just set:

```python
private_key = "0xYOUR_KEY_HERE"
```

6. Run

```
python deploy.py
```

To run on a testnet, just change these variables to whatever testnet you want to work with:

```
w3 = Web3(Web3.HTTPProvider("http://127.0.0.1:8545" || "https://sepolia.infura.io/v3/API_KEY_PROJECT"))
chaind_id = 1337
my_address = "0x94B806BB0e455576ea46193D9DBbB08d1cc57Da9"
private_key = os.getenv("PRIVATE_KEY")
```

And make sure you have testnet ETH for whatever testnet you're on!
