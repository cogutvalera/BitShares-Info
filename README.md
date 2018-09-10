______________________________________________________________________________________________________________________
# My BitShares Core Issues (28-29 weeks progress)

1. https://github.com/bitshares/bitshares-core/issues/809 / https://github.com/bitshares/bitshares-core/pull/1102 / https://github.com/bitshares/bitshares-fc/pull/56 (2 hours estimation, closed, compensated 28-29 weeks)

2. https://github.com/bitshares/bitshares-core/issues/929 / https://github.com/bitshares/bitshares-fc/pull/62 (2 hours estimation, closed, compensated 28-29 weeks)

3. https://github.com/bitshares/bitshares-core/issues/1050 / https://github.com/bitshares/bitshares-core/pull/1104 / https://github.com/bitshares/bitshares-fc/pull/63 (4 hours estimation, closed, compensated 28-29 weeks)

4. https://github.com/bitshares/bitshares-core/issues/1135 / https://github.com/bitshares/bitshares-core/pull/1153 / https://github.com/bitshares/bitshares-core/pull/1154 (30 mins estimation, closed, compensated 28-29 weeks)

5. https://github.com/bitshares/bitshares-core/issues/688 / https://github.com/bitshares/bitshares-core/pull/1159 (30 mins estimation, closed, compensated 28-29 weeks)

______________________________________________________________________________________________________________________
# My BitShares Core Issues (30-31 weeks progress)

1. https://github.com/bitshares/bitshares-core/issues/597 / https://github.com/bitshares/bitshares-fc/pull/67 (1 hour estimation, closed, compensated 30-31 weeks)

2. https://github.com/bitshares/bitshares-core/issues/1193 / https://github.com/bitshares/bitshares-core/pull/1207 / https://github.com/bitshares/bitshares-fc/pull/68 / https://github.com/bitshares/bitshares-fc/pull/70 / https://github.com/bitshares/bitshares-core/pull/1232 (7 hours estimation, NOT CLOSED, compensated 30-31 weeks)

3. https://github.com/bitshares/bitshares-core/issues/1216 / https://github.com/bitshares/bitshares-core/pull/1218 / https://github.com/bitshares/bitshares-fc/pull/71 (4 hours estimation, closed-reverted-unmerged)

______________________________________________________________________________________________________________________
# My BitShares Core Issues (34-35 weeks progress)

1. https://github.com/bitshares/bitshares-core/issues/1192 / https://github.com/bitshares/bitshares-core/pull/1243 (10 hours estimation, merged)

2. https://github.com/bitshares/bitshares-core/issues/1109 / https://github.com/bitshares/bitshares-core/pull/1195 (3 hours estimation, closed, merged)

______________________________________________________________________________________________________________________
# My BitShares Core Issues (36-37 weeks progress)

1. https://github.com/bitshares/bitshares-core/issues/780 / https://github.com/bitshares/bitshares-core/pull/1174 (5 hours estimation, review required)

2. https://github.com/bitshares/bitshares-core/issues/1171 (in progress)

3. https://github.com/bitshares/bitshares-core/issues/1303 (10 hours estimation, in progress)

4. https://github.com/bitshares/bitshares-core/issues/777 (in progress)

5. https://github.com/bitshares/bitshares-core/issues/946 / https://github.com/bitshares/bitshares-core/pull/1311 (2 hours estimation, review required)

6. https://github.com/bitshares/bitshares-core/issues/1313

7. https://github.com/bitshares/bitshares-core/issues/1314

______________________________________________________________________________________________________________________
# My BitShares Core Issues

1. https://github.com/bitshares/bitshares-core/issues/1088 ???

2. https://github.com/bitshares/bitshares-core/issues/774

3. https://github.com/bitshares/bitshares-core/issues/1205 (closed, NOT ISSUE)

4. https://github.com/bitshares/bitshares-core/issues/726

5. https://github.com/bitshares/bitshares-core/issues/1288

6. https://github.com/bitshares/bitshares-core/issues/964

7. https://github.com/bitshares/bitshares-core/issues/1233

______________________________________________________________________________________________________________________

# Discussions

https://github.com/bitshares/bitshares-core/pulls?q=is%3Apr+milestone%3A%22201807+-+Next+Non-Consensus-Changing+Release%22+is%3Aopen

1. https://github.com/bitshares/bitshares-core/pull/1120
2. https://github.com/bitshares/bitshares-core/pull/952
3. https://github.com/bitshares/bitshares-core/issues/1172
4. https://github.com/bitshares/bitshares-core/issues/1173
5. https://github.com/bitshares/bitshares-core/issues/1182
6. https://github.com/bitshares/bitshares-core/issues/1237
7. https://github.com/bitshares/bitshares-core/issues/1245
8. https://github.com/bitshares/bitshares-core/pull/1250
9. https://github.com/bitshares/bitshares-core/pull/406
10. https://github.com/bitshares/bitshares-core/pull/1049
11. https://github.com/bitshares/bitshares-core/pull/915
12. https://github.com/bitshares/bitshares-core/issues/363
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

2. https://github.com/bitshares/bitshares-ui/issues/1762

3. https://github.com/bitshares/bitshares-ui/issues/1770

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

# Buy Servers info

1. https://www.hetzner.com/?country=us

Intel® Core™ i7-8700 Hexa-Core Coffee Lake
2 x 512 gb NVMe SSDs in RAID
64GB ram

2. https://bitsharestalk.org/index.php?topic=24046.msg305206#msg305206
3. https://bitsharestalk.org/index.php/topic,24005.0.html
4. https://bitsharestalk.org/index.php/topic,23925.0.html
______________________________________________________________________________________________________________________

# Forum Discussions

1. http://bitsharestalk.org/index.php?topic=26906.0
2. http://bitsharestalk.org/index.php?topic=26907.0
______________________________________________________________________________________________________________________

# Others Info

1. https://learn.javascript.ru/write-unmain-code
2. https://forum.unity.com/threads/facebook-unity-settings-has-already-been-imported-error.467925/
3. https://www.investopedia.com
4. https://steemit.com/bitshares/@malacandrahyoi/stealth-on-bitshares-development-phase-ii
5. https://medium.com/@bytemaster/proposal-for-eos-resource-renting-rent-distribution-9afe8fb3883a
6. https://www.investopedia.com/terms/c/corporategovernance.asp
7. https://steemit.com/bitshares/@blockchained/sostoyanie-seti-bitshares-7-avgusta-2018
8. https://steemit.com/blockchain/@blockchained/tobi-linas-o-bookiepro-pervoi-v-mire-decentralizovannoi-birzhe-sportivnykh-stavok
9. https://www.youtube.com/watch?v=XQ916ga2uqg
10. https://docs.microsoft.com/en-us/cpp/cpp/cpp-language-reference

______________________________________________________________________________________________________________________

# BitShares + Telegram Bot

1. https://gitlab.com/dmantis/bitshares-assistant

______________________________________________________________________________________________________________________

in general I hope you will review the Project Backlog to identify Unassigned - Bugs then Unassigned - Features & Enhancements (rather than New - Awaiting Core Team Evaluation. As a Team, we are working to prioritize the Issues within each bucket (column heading). We also use the 4 Priority Labels to help as well. If you are unable to find an Unassigned Issue, please look to the New Issues and reach out to me. I can work with the Core Team to review, prioritize and estimate Issues which Community Members have interest in working on.

______________________________________________________________________________________________________________________

# TODO

1. C++
2. Design Patterns
3. Economics
4. Graphene
5. BitShares-Core
6. Tanenbaum Architecture
7. Tanenbaum Networks
8. Tanenbaum Operating Systems

______________________________________________________________________________________________________________________
