# NEW DATA USING MAINNET/REAL FIGURES #
```
oldEpochLength=30000
newEpochLength=60000
ETCHASH_FORK_BLOCK=11460000
```
```
$ ./geth-1.11.13 makecache 11459999 ../caches/old/
INFO [09-14|19:33:51.021] Generating ethash verification cache     epoch=381 percentage=54 elapsed=3.001s
INFO [09-14|19:33:53.502] Generated ethash verification cache      epoch=381 elapsed=5.482s
$ ./geth-1.11.13 makecache 11460000 ../caches/old/
INFO [09-14|19:34:30.398] Generating ethash verification cache     epoch=382 percentage=52 elapsed=3.000s
INFO [09-14|19:34:33.208] Generated ethash verification cache      epoch=382 elapsed=5.810s
```
```
$ ls -lh ../caches/old
total 128M
-rw-rw-r-- 1 xocel xocel 64M sep 14 19:33 cache-R23-b66c92ab2a9866c1
-rw-rw-r-- 1 xocel xocel 64M sep 14 19:34 cache-R23-d3d0aa11197dcdcf

$ sha256sum ../caches/old/*
2502c63d8e89ae5ab4ac9e2d353b458effd46ad5f1f18cd7b66491856014aa3d  ../caches/old/cache-R23-b66c92ab2a9866c1
c94310316f18c37eee7cb04b6b7a4b1ccef617f8879a8c8cfd4e0d3dd34aebce  ../caches/old/cache-R23-d3d0aa11197dcdcf
```
```
$ ./geth-etchash makecache 11459999 ../caches/new/
INFO [09-14|19:35:13.953] Generating ethash verification cache     epoch=381 epochLength=30000 percentage=54 elapsed=3.002s
INFO [09-14|19:35:16.552] Generated ethash verification cache      epoch=381 epochLength=30000 elapsed=5.601s
$ ./geth-etchash makecache 11460000 ../caches/new/
INFO [09-14|19:35:38.191] Generating ethash verification cache     epoch=191 epochLength=60000 percentage=85 elapsed=3.001s
INFO [09-14|19:35:38.691] Generated ethash verification cache      epoch=191 epochLength=60000 elapsed=3.501s
```
```
$ ls -lh ../caches/new
total 104M
-rw-rw-r-- 1 xocel xocel 64M sep 14 19:35 cache-R23-b66c92ab2a9866c1
-rw-rw-r-- 1 xocel xocel 40M sep 14 19:35 cache-R23-d3d0aa11197dcdcf

$ sha256sum ../caches/new/*
2502c63d8e89ae5ab4ac9e2d353b458effd46ad5f1f18cd7b66491856014aa3d  ../caches/new/cache-R23-b66c92ab2a9866c1
9b26943b372f61f6b16674f55b1ad2d072f9058bf7c1b6a3065d4d8f8f8143e9  ../caches/new/cache-R23-d3d0aa11197dcdcf
```
# DATASETS 
```
$ ./geth-1.11.13 makedag 11459999 ../dags/old/       
INFO [09-14|19:41:12.577] Generating ethash verification cache     epoch=381 percentage=57 elapsed=3.000s
INFO [09-14|19:41:14.866] Generated ethash verification cache      epoch=381 elapsed=5.289s
INFO [09-14|19:41:18.181] Generating DAG in progress               epoch=381 percentage=0  elapsed=3.314s

$ ./geth-1.11.13 makedag 11460000 ../dags/old/
INFO [09-14|19:47:21.859] Generating ethash verification cache     epoch=382 percentage=57 elapsed=3.001s
INFO [09-14|19:47:24.126] Generated ethash verification cache      epoch=382 elapsed=5.269s
INFO [09-14|19:47:27.337] Generating DAG in progress               epoch=382 percentage=0  elapsed=3.210s
```
```
$ ls -lh ../dags/old/
total 8,0G
-rw-rw-r-- 1 xocel xocel 4,0G sep 14 19:46 full-R23-b66c92ab2a9866c1
-rw-rw-r-- 1 xocel xocel 4,0G sep 14 19:54 full-R23-d3d0aa11197dcdcf

$ sha256sum ../dags/old/*
48eb68514f5f201bdf4fc96840f691a09b5a644ef3e3a9fd92df4aff7951249a  ../dags/old/full-R23-b66c92ab2a9866c1
98c3fbf40ac51462c2fd97e14fcdbea1e5521b5cd39874997efa091cc821fd77  ../dags/old/full-R23-d3d0aa11197dcdcf
```
```
$ ./geth-etchash makedag 11459999 ../dags/new/
INFO [09-14|20:00:11.990] Generating ethash verification cache     epoch=381 epochLength=30000 percentage=51 elapsed=3.002s
INFO [09-14|20:00:14.905] Generated ethash verification cache      epoch=381 epochLength=30000 elapsed=5.916s
INFO [09-14|20:00:18.395] Generating DAG in progress               epoch=381 epochLength=30000 percentage=0  elapsed=3.489s

$ ./geth-etchash makedag 11460000 ../dags/new/
INFO [09-14|20:07:21.533] Generating ethash verification cache     epoch=191 epochLength=60000 percentage=89 elapsed=3.000s
INFO [09-14|20:07:21.871] Generated ethash verification cache      epoch=191 epochLength=60000 elapsed=3.338s
INFO [09-14|20:07:23.974] Generating DAG in progress               epoch=191 epochLength=60000 percentage=0  elapsed=2.103s
```
```
$ ls -lh ../dags/new/
total 6,5G
-rw-rw-r-- 1 xocel xocel 4,0G sep 14 20:06 full-R23-b66c92ab2a9866c1
-rw-rw-r-- 1 xocel xocel 2,5G sep 14 20:11 full-R23-d3d0aa11197dcdcf

$ sha256sum ../dags/new/*
48eb68514f5f201bdf4fc96840f691a09b5a644ef3e3a9fd92df4aff7951249a  ../dags/new/full-R23-b66c92ab2a9866c1
e4393f85ba2ea69b4bcfaabd0ada1428e48f15738ee5beb1983439433bb86e49  ../dags/new/full-R23-d3d0aa11197dcdcf
```
