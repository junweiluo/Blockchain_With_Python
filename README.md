# Blockchain_With_Python

# What is an HD Wallet?

An HD Wallet, or Hierachical Deterministic wallet, is a new-age digital wallet that automaticvally generates a hierarchical tree-like structure of private/public address or keys, thereby addressing the problem of the user having to generate them on their own.

# Derive a HD Wallet

This is in wallet.py of function 'derive_wallet':

command = f'./derive -g --mnemonic="{mnemonic}" --coin="{coin}" --numderive="{num}" --cols=index,path,address,privkey,pubkey,pubkeyhash,xprv,xpub --format=json'

There will be 8 fiels in each derive. 

# Exectuting from terminal to send transactions using commends below.

from wallet import *

btc_acc = priv_key_account(BTCTEST, derive_wallets(mnemonic, BTCTEST,5)[0]['privkey'])

eth_acc = priv_key_account(ETH, derive_wallets(mnemonic, ETH,5)[0]['privkey'])

send_tx(BTCTEST, btc_acc, derive_wallets(mnemonic, BTCTEST, 5)[1]['address'], 0.001)

send_tx(ETH, eth_acc, derive_wallets(mnemonic, ETH, 5)[1]['address'], 1000)

# Proof of Transactions

![](https://github.com/junweiluo/Blockchain_With_Python/blob/master/Screenshots/Screen%20Shot%202020-05-09%20at%205.37.03%20PM.png)

![](https://github.com/junweiluo/Blockchain_With_Python/blob/master/Screenshots/Screen%20Shot%202020-05-09%20at%205.37.39%20PM.png)

![](https://github.com/junweiluo/Blockchain_With_Python/blob/master/Screenshots/Screen%20Shot%202020-05-09%20at%207.45.18%20PM.png)
