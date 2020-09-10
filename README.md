# ecip-1099-data
Research/Test data related to ecip-1099

### Test case ###

For testing purposes a modified client using epochLength=100 has been used to save time.
This differs from mainnet which uses epochLength=30000.

NOTES-old: 10 epochs (100blocks each), representing vanilla/unmodified rules. the activation block was set to block 2000 (thus never reached)
NOTES-new: Begins with epochLength=100, at block 400 activates ecip-xxxx (epochLength=200)

The caches and dags are not included due to filesize.

### Observations ###

In the test case

old epoch 4
```
old seed[:6]           : b903bd
old size (cache)       : 17301064
old size (dataset)     : 1107293064
sha256sum[:6] (cache)  : 72c3d6
sha256sum[:6] (dataset): 8c2bcc
```
old epoch 8
```
old seed[:6]           : c307e5
old size (cache)       : 17824200
old size (dataset)     : 1140849544
sha256sum[:6] (cache)  : 0f1c6d3
sha256sum[:6] (dataset): 678c68
```
old epoch 9
```
old seed[:6]           : ec9d54
old size (cache)       : 17955912
old size (dataset)     : 1149232776
sha256sum[:6] (cache)  : 8525b7
sha256sum[:6] (dataset): f65bea
```
new epoch 8/4b
```
new seed[:6]           : c307e5
new size (cache)       : 17301064
new size (dataset)     : 1107293064
sha256sum[:6] (cache)  : 4f3f0c
sha256sum[:6] (dataset): 00b7ca
```

### conclusion ###

The current implementation is behaving as intended. Epoch with seed c307e5 (8 on vanilla, 4b on activated) has the seed of Epoch 8, but both the cache and dataset size of Epoch 4 (vanilla: b903bd). Seeds are being produced using oldEpochLength, while everywhere else is using newEpochLength after activation. Both existing and future DAG growth are halved, while ensuring seeds are not re-used.

### implementation ###

For a the smoothest possible transition activation should occur on an epoch transition in which the 'new' epoch divides by 2 cleanly. e.g

epoch 374/2 = 187 (good)
epoch 375/2 = 187.5 (bad)
epoch 376/2 = 188 (good)

activationBlock = epoch * oldEpochLength
activationBlock = 376*30000 = 11280000

Example activation at block 11280000 (epoch 376)

(Without activation)
Block: 11280000
Epoch: 376
DAG size: 3.94GB

(With activation)
Block: 11280000
Epoch: 188(b)
DAG size: 2.47GB

Using 12.6s for avg blocktime, the reduced growth results in ~334mb per year to DAG. Adding ~4years of 4GB GPU support.
