### method ###

data is based on initial epoch length of 100blocks, hardfork block 400, changing epoch length to 200 blocks.

see NOTES-old for vanilla data.

### DAG CACHES ###
```
$ ./build/bin/geth makecache 99 research/caches/new/
INFO [09-08|17:34:24.593] ecipIquidus1                             block=99 epochLength=100 epoch=0
INFO [09-08|17:34:24.594] ecipIquidus1                             block=1  epochLength=100 epoch=0
$ ./build/bin/geth makecache 199 research/caches/new/
INFO [09-08|17:34:29.932] ecipIquidus1                             block=199 epochLength=100 epoch=1
INFO [09-08|17:34:29.932] ecipIquidus1                             block=101 epochLength=100 epoch=1
$ ./build/bin/geth makecache 299 research/caches/new/
INFO [09-08|17:34:36.369] ecipIquidus1                             block=299 epochLength=100 epoch=2
INFO [09-08|17:34:36.369] ecipIquidus1                             block=201 epochLength=100 epoch=2
$ ./build/bin/geth makecache 399 research/caches/new/
INFO [09-08|17:34:41.529] ecipIquidus1                             block=399 epochLength=100 epoch=3
INFO [09-08|17:34:41.529] ecipIquidus1                             block=301 epochLength=100 epoch=3
$ ./build/bin/geth makecache 499 research/caches/new/
INFO [09-08|17:34:47.661] ecipIquidus1                             block=499 epochLength=200 epoch=2
INFO [09-08|17:34:47.662] ecipIquidus1                             block=401 epochLength=200 epoch=2
$ ./build/bin/geth makecache 599 research/caches/new/
INFO [09-08|17:34:53.281] ecipIquidus1                             block=599 epochLength=200 epoch=2
INFO [09-08|17:34:53.281] ecipIquidus1                             block=401 epochLength=200 epoch=2
$ ./build/bin/geth makecache 699 research/caches/new/
INFO [09-08|17:34:57.993] ecipIquidus1                             block=699 epochLength=200 epoch=3
INFO [09-08|17:34:57.993] ecipIquidus1                             block=601 epochLength=200 epoch=3
$ ./build/bin/geth makecache 799 research/caches/new/
INFO [09-08|17:35:03.887] ecipIquidus1                             block=799 epochLength=200 epoch=3
INFO [09-08|17:35:03.887] ecipIquidus1                             block=601 epochLength=200 epoch=3
$ ./build/bin/geth makecache 899 research/caches/new/
INFO [09-08|17:35:09.452] ecipIquidus1                             block=899 epochLength=200 epoch=4
INFO [09-08|17:35:09.453] ecipIquidus1                             block=801 epochLength=200 epoch=4
$ ./build/bin/geth makecache 999 research/caches/new/
INFO [09-08|17:35:15.940] ecipIquidus1                             block=999 epochLength=200 epoch=4
INFO [09-08|17:35:15.940] ecipIquidus1                             block=801 epochLength=200 epoch=4

0:000000 (0 )
1:290dec (1 )
2:510e4e (2a)
3:356e5a (3a)
4:b903bd (2b)
5: -
6:582b06 (3b)
7: -
8:c307e5 (4b)
9: -

$ sha256sum ./research/caches/new/*
84e99ec640a1cad132c3801b66ffbf744a74945a0a2917eeb97e156604e70aa7  ./research/caches/new/cache-R23-0000000000000000
7d1a5f589211f36220070fa0c47e69e4d3319755332abd753be8eedfb4e33937  ./research/caches/new/cache-R23-290decd9548b62a8
e98ab072b2d74e414d3e3746fbb90d48d72adf64170f896e3ba95748ad463850  ./research/caches/new/cache-R23-510e4e770828ddbf
e49cc32cbb2bbfddb8993d9b444bc2f7f79df172663ed4d85d1eb811fc940852  ./research/caches/new/cache-R23-356e5a2cc1eba076
f7441acca8204eef98a96f39b0e29d49a5263fa8bb104fe225cb1a86dc1ef594  ./research/caches/new/cache-R23-b903bd7696740696
1bb5c785b2551a30af46a1e0d13e272e9688681a16b8b98453373912a02a1d14  ./research/caches/new/cache-R23-582b06447f087674
4f3f0ce3295e497a8613830a4e73b0d6df8c87266cffc9f63061499aa8862fed  ./research/caches/new/cache-R23-c307e5620454e771

$ ls -l research/caches/new/*
-rw-rw-r-- 1 xocel xocel 16776904 sep  8 17:34 research/caches/new/cache-R23-0000000000000000
-rw-rw-r-- 1 xocel xocel 16907464 sep  8 17:34 research/caches/new/cache-R23-290decd9548b62a8
-rw-rw-r-- 1 xocel xocel 17039304 sep  8 17:34 research/caches/new/cache-R23-510e4e770828ddbf
-rw-rw-r-- 1 xocel xocel 17170120 sep  8 17:34 research/caches/new/cache-R23-356e5a2cc1eba076
-rw-rw-r-- 1 xocel xocel 17039304 sep  8 17:34 research/caches/new/cache-R23-b903bd7696740696
-rw-rw-r-- 1 xocel xocel 17170120 sep  8 17:34 research/caches/new/cache-R23-582b06447f087674
-rw-rw-r-- 1 xocel xocel 17301064 sep  8 17:35 research/caches/new/cache-R23-c307e5620454e771

### DAG DATASETS ###

$ ./build/bin/geth makedag 99 research/dags/new/
INFO [09-08|17:38:04.366] ecipIquidus1                             block=99 epochLength=100 epoch=0
INFO [09-08|17:38:04.366] ecipIquidus1                             block=1  epochLength=100 epoch=0
$ ./build/bin/geth makedag 199 research/dags/new/
INFO [09-08|17:39:41.515] ecipIquidus1                             block=199 epochLength=100 epoch=1
INFO [09-08|17:39:41.515] ecipIquidus1                             block=101 epochLength=100 epoch=1
$ ./build/bin/geth makedag 299 research/dags/new/
INFO [09-08|17:41:12.210] ecipIquidus1                             block=299 epochLength=100 epoch=2
INFO [09-08|17:41:12.211] ecipIquidus1                             block=201 epochLength=100 epoch=2
$ ./build/bin/geth makedag 399 research/dags/new/
INFO [09-08|17:41:12.210] ecipIquidus1                             block=399 epochLength=100 epoch=3
INFO [09-08|17:41:12.211] ecipIquidus1                             block=301 epochLength=100 epoch=3
$ ./build/bin/geth makedag 499 research/dags/new/
INFO [09-08|17:44:44.557] ecipIquidus1                             block=499 epochLength=200 epoch=2
INFO [09-08|17:44:44.557] ecipIquidus1                             block=401 epochLength=200 epoch=2
$ ./build/bin/geth makedag 599 research/dags/new/
INFO [09-08|17:46:36.572] ecipIquidus1                             block=599 epochLength=200 epoch=2
INFO [09-08|17:46:36.572] ecipIquidus1                             block=401 epochLength=200 epoch=2
$ ./build/bin/geth makedag 699 research/dags/new/
INFO [09-08|17:47:06.374] ecipIquidus1                             block=699 epochLength=200 epoch=3
INFO [09-08|17:47:06.374] ecipIquidus1                             block=601 epochLength=200 epoch=3
ev@octano:~$ ./build/bin/geth makedag 799 research/dags/new/
INFO [09-08|17:50:36.623] ecipIquidus1                             block=799 epochLength=200 epoch=3
INFO [09-08|17:50:36.623] ecipIquidus1                             block=601 epochLength=200 epoch=3
$ ./build/bin/geth makedag 899 research/dags/new/
INFO [09-08|17:51:00.292] ecipIquidus1                             block=899 epochLength=200 epoch=4
INFO [09-08|17:51:00.292] ecipIquidus1                             block=801 epochLength=200 epoch=4

0:000000 (0 )
1:290dec (1 )
2:510e4e (2a)
3:356e5a (3a)
4:b903bd (2b)
5: -
6:582b06 (3b)
7: -
8:c307e5 (4b)
9: -

$ sha256sum research/dags/new/*
eeea94d40618f94590f470771dd2dbcd8390dc2c2b6029519d3c2b65f807be1b  research/dags/new/full-R23-0000000000000000
49d6581c6e8d278eb4c470e9a64d8ca880259b28325975a154a1eb53f5ac9573  research/dags/new/full-R23-290decd9548b62a8
e6c3bb360cf47487c2e62ba2ca2aa636852732679457db93d4ed0a0dcc71679c  research/dags/new/full-R23-510e4e770828ddbf
cc3ce58de83fb96ebe890c2f60d2c1eba160884168b7b19dba72c6565dfe89b8  research/dags/new/full-R23-356e5a2cc1eba076
93603720ac24ebd4fd48849279108801dba15a21badc66f2bad830431b8e8f08  research/dags/new/full-R23-b903bd7696740696
398b84d92fb6f8c891c10c41286a26c0454c19c5c180ae2b0de6b5a4c4c1dfae  research/dags/new/full-R23-582b06447f087674
00b7ca5cc65f9b915c9a49ed556bef75f0993bf90bd56b1c0516d4e081487df0  research/dags/new/full-R23-c307e5620454e771

$ ls -l research/dags/new/*
-rw-rw-r-- 1 xocel xocel 1073739912 sep  8 17:39 research/dags/new/full-R23-0000000000000000
-rw-rw-r-- 1 xocel xocel 1082130312 sep  8 17:41 research/dags/new/full-R23-290decd9548b62a8
-rw-rw-r-- 1 xocel xocel 1090514824 sep  8 17:42 research/dags/new/full-R23-510e4e770828ddbf
-rw-rw-r-- 1 xocel xocel 1098906760 sep  8 17:44 research/dags/new/full-R23-356e5a2cc1eba076
-rw-rw-r-- 1 xocel xocel 1090514824 sep  8 17:46 research/dags/new/full-R23-b903bd7696740696
-rw-rw-r-- 1 xocel xocel 1098906760 sep  8 17:49 research/dags/new/full-R23-582b06447f087674
-rw-rw-r-- 1 xocel xocel 1107293064 sep  8 17:52 research/dags/new/full-R23-c307e5620454e771
```
