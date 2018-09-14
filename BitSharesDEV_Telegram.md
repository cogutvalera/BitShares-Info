```
Ryan R. Fox (BitShares Core), [14.09.18 15:09]
May I request some assistance with the following questions:

Q: What is the maximum number of operations within a single transaction? (Is there a fixed number per transaction/block or limited by any other factors such as transaction/block size in bytes)
Q: When is signature validation performed by a validation node? (Before broadcasting on the P2P or only by the BP after receipt)
Q:What is the order of validation operations performed by validation nodes when receiving a block through the P2P?

Alex M - clockwork, [14.09.18 15:10]
[In reply to Ryan R. Fox (BitShares Core)]
1.  Limited by max block-size (adjustable by committee).

Abit More, [14.09.18 15:11]
[In reply to Ryan R. Fox (BitShares Core)]
1. TRX size and block size.

Abit More, [14.09.18 15:16]
[In reply to Ryan R. Fox (BitShares Core)]
2. for new transactions, will validate after received, before broadcast;
for new blocks, signature of blocks will be validated when received;
for transactions in blocks: if enabled witness plugin or node is started with --force-validate option, will validate when received the block; otherwise, will skip the validation for better performance.

Abit More, [14.09.18 15:17]
[In reply to Ryan R. Fox (BitShares Core)]
3. I don't really understand the question

Ryan R. Fox (BitShares Core), [14.09.18 15:22]
3: trying to understand when a broadcast TX received from P2P get validated. My assumption: TX rcvd, check sig, check operations, validated, add to mempool, await block containing TX, remove from mempool after LIB.

Peter Conrad, [14.09.18 15:26]
Incoming new transactions are pushed into the database. Same validation steps are applied as for those transactions that arrive in a new block.
TX's are kept in pool until their expiration date, for dupe checking.

Ryan R. Fox (BitShares Core), [14.09.18 15:28]
[In reply to Peter Conrad]
Good point. LIB as I described would allow replay same TX.

Abit More, [14.09.18 15:58]
[In reply to Ryan R. Fox (BitShares Core)]
dup check is not related to LIB

Abit More, [14.09.18 15:59]
effectively there are two pools. one for dup check, the other for propagating among peers

Abit More, [14.09.18 16:02]
actually, one pool in database for dup check, one pool in p2p layer for propagating. there is a fork db and a pending queue in database, to assist the dup check and chain reoganization and block production.
```
