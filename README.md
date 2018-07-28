# My BitShares Core Issues

1. https://github.com/bitshares/bitshares-core/issues/809 / https://github.com/bitshares/bitshares-core/pull/1102 / https://github.com/bitshares/bitshares-fc/pull/56 (2 hours estimation, closed)

2. https://github.com/bitshares/bitshares-core/issues/929 / https://github.com/bitshares/bitshares-fc/pull/62 (2 hours estimation, closed)

3. https://github.com/bitshares/bitshares-core/issues/1050 / https://github.com/bitshares/bitshares-core/pull/1104 / https://github.com/bitshares/bitshares-fc/pull/63 (4 hours estimation, closed)

4. https://github.com/bitshares/bitshares-core/issues/1088 ???

5. https://github.com/bitshares/bitshares-core/issues/946 ???

6. https://github.com/bitshares/bitshares-core/issues/777 ???

7. https://github.com/bitshares/bitshares-core/issues/1135 / https://github.com/bitshares/bitshares-core/pull/1153 / https://github.com/bitshares/bitshares-core/pull/1154 (30 mins estimation, closed)

8. https://github.com/bitshares/bitshares-core/issues/688 / https://github.com/bitshares/bitshares-core/pull/1159 (30 mins estimation, closed)

9. https://github.com/bitshares/bitshares-core/issues/597 / https://github.com/bitshares/bitshares-fc/pull/67 (1 hour estimation)

10. https://github.com/bitshares/bitshares-core/issues/780 / https://github.com/bitshares/bitshares-core/pull/1174 (2 hours estimation)

11. https://github.com/bitshares/bitshares-core/issues/1192

12. https://github.com/bitshares/bitshares-core/issues/1109 / https://github.com/bitshares/bitshares-core/pull/1195

13. https://github.com/bitshares/bitshares-core/issues/1193

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
