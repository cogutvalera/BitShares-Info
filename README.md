# My BitShares Core Issues

1. https://github.com/bitshares/bitshares-core/issues/809 / https://github.com/bitshares/bitshares-core/pull/1102 / https://github.com/bitshares/bitshares-fc/pull/56 (2 hours estimation, closed, compensated)

2. https://github.com/bitshares/bitshares-core/issues/929 / https://github.com/bitshares/bitshares-fc/pull/62 (2 hours estimation, closed, compensated)

3. https://github.com/bitshares/bitshares-core/issues/1050 / https://github.com/bitshares/bitshares-core/pull/1104 / https://github.com/bitshares/bitshares-fc/pull/63 (4 hours estimation, closed, compensated)

4. https://github.com/bitshares/bitshares-core/issues/1088 ???

5. https://github.com/bitshares/bitshares-core/issues/946 ???

6. https://github.com/bitshares/bitshares-core/issues/777 ???

7. https://github.com/bitshares/bitshares-core/issues/1135 / https://github.com/bitshares/bitshares-core/pull/1153 / https://github.com/bitshares/bitshares-core/pull/1154 (30 mins estimation, closed, compensated)

8. https://github.com/bitshares/bitshares-core/issues/688 / https://github.com/bitshares/bitshares-core/pull/1159 (30 mins estimation, closed, compensated)

9. https://github.com/bitshares/bitshares-core/issues/597 / https://github.com/bitshares/bitshares-fc/pull/67 (1 hour estimation, closed)

10. https://github.com/bitshares/bitshares-core/issues/780 / https://github.com/bitshares/bitshares-core/pull/1174 (2 hours estimation)

11. https://github.com/bitshares/bitshares-core/issues/1192

12. https://github.com/bitshares/bitshares-core/issues/1109 / https://github.com/bitshares/bitshares-core/pull/1195 (2 hours estimation)

13. https://github.com/bitshares/bitshares-core/issues/1193 (2-3 hours estimation)

14. https://github.com/bitshares/bitshares-core/issues/1205 (closed, NOT ISSUE)

______________________________________________________________________________________________________________________

# Discussions

https://github.com/bitshares/bitshares-core/pulls?q=is%3Apr+milestone%3A%22201807+-+Next+Non-Consensus-Changing+Release%22+is%3Aopen

1. https://github.com/bitshares/bitshares-core/pull/1120

2. https://github.com/bitshares/bitshares-core/pull/952

3. https://github.com/bitshares/bitshares-core/issues/1172

4. https://github.com/bitshares/bitshares-core/issues/1173

5. https://github.com/bitshares/bitshares-core/issues/1182

______________________________________________________________________________________________________________________

# BSIPs

1. https://github.com/bitshares/bsips/pull/84

______________________________________________________________________________________________________________________

# NOTES

## Steps to bump FC Library

```
cd bitshares-core
cd libraries
rm -rf fc
git submodule update --init --recursive
cd fc
git fetch origin
git checkout origin/master
git submodule update --init --recursive
cd ..
git add fc
git commit
```
______________________________________________________________________________________________________________________

# BitShares UI issues

1. https://github.com/bitshares/bitshares-ui/issues/1729


______________________________________________________________________________________________________________________

# BitShares run tests

1. ./tests/all_tests --run_test=logging_tests/log_reboot --log_level=message

______________________________________________________________________________________________________________________

# Private TestNet How To:

http://docs.bitshares.org/testnet/private-testnet.html

```
$ witness_node --create-genesis-json=my-genesis.json
witness_node --data-dir=data   # to use the default genesis, or
witness_node --data-dir=data --genesis-json=my-genesis.json   # your own genesis block

[Testnet-Home]/data/config.ini:
rpc-endpoint = 127.0.0.1:8090
genesis-json = my-genesis.json
enable-stale-production = true
# ID of witness controlled by this node (e.g. "1.6.5", quotes are required, may specify multiple times)
witness-id = "1.6.1"
witness-id = "1.6.2"
witness-id = "1.6.3"
witness-id = "1.6.4"
witness-id = "1.6.5"
witness-id = "1.6.6"
witness-id = "1.6.7"
witness-id = "1.6.8"
witness-id = "1.6.9"
witness-id = "1.6.10"
witness-id = "1.6.11"
# Tuple of [PublicKey, WIF private key] (may specify multiple times)
private-key = ["BTS6MRyA...T5GDW5CV","5KQwrPb...tP79zkvFD3"]
seed-nodes = []

witness_node --data-dir=data

cli_wallet --wallet-file=my-wallet.json --chain-id=8b7bd36a146a03d0e5d0a971e286098f41230b209d96f92465cd62bd64294824 --server-rpc-endpoint=ws://127.0.0.1:8090
```
______________________________________________________________________________________________________________________
