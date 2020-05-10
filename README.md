# Blockchain_With_Python

What is an HD Wallet?

An HD Wallet, or Hierachical Deterministic wallet, is a new-age digital wallet that automaticvally generates a hierarchical tree-like structure of private/public address or keys, thereby addressing the problem of the user having to generate them on their own.

from wallet import *
btc_acc = priv_key_account(BTCTEST, derive_wallets(mnemonic, BTCTEST,5)[0]['privkey'])
eth_acc = priv_key_account(ETH, derive_wallets(mnemonic, ETH,5)[0]['privkey'])
send_tx(BTCTEST, btc_acc, derive_wallets(mnemonic, BTCTEST, 5)[1]['address'], 0.001)
send_tx(ETH, eth_acc, derive_wallets(mnemonic, ETH, 5)[1]['address'], 1000)
