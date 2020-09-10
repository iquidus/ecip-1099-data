### method ###

data is based on initial epoch length of 100blocks

see NOTES-new for ecip-xxxx activated data.

### DAG CACHES ###
```
$ ./build/bin/geth makecache 99 research/caches/old/  
INFO [09-08|19:35:18.272] ecipIquidus1                             block=99 epochLength=100 epoch=0
INFO [09-08|19:35:18.272] ecipIquidus1                             block=1  epochLength=100 epoch=0
$ ./build/bin/geth makecache 199 research/caches/old/
INFO [09-08|19:35:39.513] ecipIquidus1                             block=199 epochLength=100 epoch=1
INFO [09-08|19:35:39.514] ecipIquidus1                             block=101 epochLength=100 epoch=1
$ ./build/bin/geth makecache 299 research/caches/old/
INFO [09-08|19:35:44.606] ecipIquidus1                             block=299 epochLength=100 epoch=2
INFO [09-08|19:35:44.606] ecipIquidus1                             block=201 epochLength=100 epoch=2
$ ./build/bin/geth makecache 399 research/caches/old/
INFO [09-08|19:35:50.096] ecipIquidus1                             block=399 epochLength=100 epoch=3
INFO [09-08|19:35:50.097] ecipIquidus1                             block=301 epochLength=100 epoch=3
$ ./build/bin/geth makecache 499 research/caches/old/
INFO [09-08|19:35:55.450] ecipIquidus1                             block=499 epochLength=100 epoch=4
INFO [09-08|19:35:55.451] ecipIquidus1                             block=401 epochLength=100 epoch=4
$ ./build/bin/geth makecache 599 research/caches/old/
INFO [09-08|19:36:01.209] ecipIquidus1                             block=599 epochLength=100 epoch=5
INFO [09-08|19:36:01.210] ecipIquidus1                             block=501 epochLength=100 epoch=5
$ ./build/bin/geth makecache 699 research/caches/old/
INFO [09-08|19:36:06.893] ecipIquidus1                             block=699 epochLength=100 epoch=6
INFO [09-08|19:36:06.893] ecipIquidus1                             block=601 epochLength=100 epoch=6
$ ./build/bin/geth makecache 799 research/caches/old/
INFO [09-08|19:36:12.135] ecipIquidus1                             block=799 epochLength=100 epoch=7
INFO [09-08|19:36:12.135] ecipIquidus1                             block=701 epochLength=100 epoch=7
$ ./build/bin/geth makecache 899 research/caches/old/
INFO [09-08|19:36:17.343] ecipIquidus1                             block=899 epochLength=100 epoch=8
INFO [09-08|19:36:17.343] ecipIquidus1                             block=801 epochLength=100 epoch=8
$ ./build/bin/geth makecache 999 research/caches/old/
INFO [09-08|19:36:25.019] ecipIquidus1                             block=999 epochLength=100 epoch=9
INFO [09-08|19:36:25.019] ecipIquidus1                             block=901 epochLength=100 epoch=9

0:000000
1:290dec
2:510e4e
3:356e5a
4:b903bd
5:f2e590
6:582b06
7:6d29f6
8:c307e5
9:ec9d54

$ sha256sum research/caches/old/*
84e99ec640a1cad132c3801b66ffbf744a74945a0a2917eeb97e156604e70aa7  research/caches/old/cache-R23-0000000000000000
7d1a5f589211f36220070fa0c47e69e4d3319755332abd753be8eedfb4e33937  research/caches/old/cache-R23-290decd9548b62a8
e98ab072b2d74e414d3e3746fbb90d48d72adf64170f896e3ba95748ad463850  research/caches/old/cache-R23-510e4e770828ddbf
e49cc32cbb2bbfddb8993d9b444bc2f7f79df172663ed4d85d1eb811fc940852  research/caches/old/cache-R23-356e5a2cc1eba076
72c3d6409b54193b01c43613db6277b12ec0e315f4435d6eb31fb24e1dd17661  research/caches/old/cache-R23-b903bd7696740696
c93386742310f66bb52a679ee30ae188b43f3d4405e1047e96f192b20c945ab4  research/caches/old/cache-R23-f2e59013a0a37983
c5b2a54a54370d3e7e386e8aca943b434af5996bd8bf6a4e74aa81888427faec  research/caches/old/cache-R23-582b06447f087674
f00858c0ae343706e9add5b18a006c859290d0b5cdef08fae03a99fb7ea5ddb3  research/caches/old/cache-R23-6d29f6dd1270e497
0f1c6d3ddf2b61a1b3611935ceb95f76c0aff12e841073b534fce5566fdddead  research/caches/old/cache-R23-c307e5620454e771
8525b716c43eada034a3116868b85c1d11080846725ded9b6785b160b7b1381b  research/caches/old/cache-R23-ec9d541d1c32bec7

$ ls -l research/caches/old/*
-rw-rw-r-- 1 xocel xocel 16776904 sep  8 19:35 research/caches/old/cache-R23-0000000000000000
-rw-rw-r-- 1 xocel xocel 16907464 sep  8 19:35 research/caches/old/cache-R23-290decd9548b62a8
-rw-rw-r-- 1 xocel xocel 17039304 sep  8 19:35 research/caches/old/cache-R23-510e4e770828ddbf
-rw-rw-r-- 1 xocel xocel 17170120 sep  8 19:35 research/caches/old/cache-R23-356e5a2cc1eba076
-rw-rw-r-- 1 xocel xocel 17301064 sep  8 19:35 research/caches/old/cache-R23-b903bd7696740696
-rw-rw-r-- 1 xocel xocel 17432520 sep  8 19:36 research/caches/old/cache-R23-f2e59013a0a37983
-rw-rw-r-- 1 xocel xocel 17563080 sep  8 19:36 research/caches/old/cache-R23-582b06447f087674
-rw-rw-r-- 1 xocel xocel 17693896 sep  8 19:36 research/caches/old/cache-R23-6d29f6dd1270e497
-rw-rw-r-- 1 xocel xocel 17824200 sep  8 19:36 research/caches/old/cache-R23-c307e5620454e771
-rw-rw-r-- 1 xocel xocel 17955912 sep  8 19:36 research/caches/old/cache-R23-ec9d541d1c32bec7

### DAG DATASETS ###

$ ./build/bin/geth makedag 99 research/dags/old/
INFO [09-08|18:10:27.861] ecipIquidus1                             block=99 epochLength=100 epoch=0
INFO [09-08|18:10:27.861] ecipIquidus1                             block=1  epochLength=100 epoch=0
$ ./build/bin/geth makedag 199 research/dags/old/
INFO [09-08|18:17:04.440] ecipIquidus1                             block=199 epochLength=100 epoch=1
INFO [09-08|18:17:04.440] ecipIquidus1                             block=101 epochLength=100 epoch=1
$ ./build/bin/geth makedag 299 research/dags/old/
INFO [09-08|18:24:46.472] ecipIquidus1                             block=299 epochLength=100 epoch=2
INFO [09-08|18:24:46.473] ecipIquidus1                             block=201 epochLength=100 epoch=2
$ ./build/bin/geth makedag 399 research/dags/old/
INFO [09-08|18:27:53.870] ecipIquidus1                             block=399 epochLength=100 epoch=3
INFO [09-08|18:27:53.871] ecipIquidus1                             block=301 epochLength=100 epoch=3
$ ./build/bin/geth makedag 499 research/dags/old/
INFO [09-08|18:30:06.251] ecipIquidus1                             block=499 epochLength=100 epoch=4
INFO [09-08|18:30:06.251] ecipIquidus1                             block=401 epochLength=100 epoch=4
$ ./build/bin/geth makedag 599 research/dags/old/
INFO [09-08|18:41:12.230] ecipIquidus1                             block=599 epochLength=100 epoch=5
INFO [09-08|18:41:12.230] ecipIquidus1                             block=501 epochLength=100 epoch=5
$ ./build/bin/geth makedag 699 research/dags/old/
INFO [09-08|18:44:44.515] ecipIquidus1                             block=699 epochLength=100 epoch=6
INFO [09-08|18:44:44.515] ecipIquidus1                             block=601 epochLength=100 epoch=6
$ ./build/bin/geth makedag 799 research/dags/old/
INFO [09-08|18:57:48.725] ecipIquidus1                             block=799 epochLength=100 epoch=7
INFO [09-08|18:57:48.725] ecipIquidus1                             block=701 epochLength=100 epoch=7
$ ./build/bin/geth makedag 899 research/dags/old/
INFO [09-08|18:59:34.270] ecipIquidus1                             block=899 epochLength=100 epoch=8
INFO [09-08|18:59:34.270] ecipIquidus1                             block=801 epochLength=100 epoch=8
$ ./build/bin/geth makedag 999 research/dags/old/
INFO [09-08|19:01:47.909] ecipIquidus1                             block=999 epochLength=100 epoch=9
INFO [09-08|19:01:47.909] ecipIquidus1                             block=901 epochLength=100 epoch=9

0:000000
1:290dec
2:510e4e
3:356e5a
4:b903bd
5:f2e590
6:582b06
7:6d29f6
8:c307e5
9:ec9d54

$ sha256sum ./research/dags/old/*
eeea94d40618f94590f470771dd2dbcd8390dc2c2b6029519d3c2b65f807be1b  ./research/dags/old/full-R23-0000000000000000
49d6581c6e8d278eb4c470e9a64d8ca880259b28325975a154a1eb53f5ac9573  ./research/dags/old/full-R23-290decd9548b62a8
e6c3bb360cf47487c2e62ba2ca2aa636852732679457db93d4ed0a0dcc71679c  ./research/dags/old/full-R23-510e4e770828ddbf
cc3ce58de83fb96ebe890c2f60d2c1eba160884168b7b19dba72c6565dfe89b8  ./research/dags/old/full-R23-356e5a2cc1eba076
8c2bcca808a0fd3db18436b5dd413caf80d43fc03d56ce704c6bba084ba978de  ./research/dags/old/full-R23-b903bd7696740696
3ece2994950557d50ca5ac2f5b0ab38f43c295cb0d308d3f929137321a5e216b  ./research/dags/old/full-R23-f2e59013a0a37983
13d46bdc2f9f3bb54ac87f2d95d88439e45bff91f564ac53a21be88f5144bd08  ./research/dags/old/full-R23-582b06447f087674
a639bd6c11ef62b9b5698bb3d0b6003b3fec3f24244b04c8f9c67d526fe05131  ./research/dags/old/full-R23-6d29f6dd1270e497
678c6835668534cb9c28187d3733eb3fae8213e34dcd5dfe59c02c8004c825b2  ./research/dags/old/full-R23-c307e5620454e771
f65beaef577f529de2835155ee7a38298398a5876460044542a535425c4a1402  ./research/dags/old/full-R23-ec9d541d1c32bec7

$ ls -l ./research/dags/old/*
-rw-rw-r-- 1 xocel xocel 1073739912 sep  8 18:11 ./research/dags/old/full-R23-0000000000000000
-rw-rw-r-- 1 xocel xocel 1082130312 sep  8 18:18 ./research/dags/old/full-R23-290decd9548b62a8
-rw-rw-r-- 1 xocel xocel 1090514824 sep  8 18:26 ./research/dags/old/full-R23-510e4e770828ddbf
-rw-rw-r-- 1 xocel xocel 1098906760 sep  8 18:29 ./research/dags/old/full-R23-356e5a2cc1eba076
-rw-rw-r-- 1 xocel xocel 1107293064 sep  8 18:31 ./research/dags/old/full-R23-b903bd7696740696
-rw-rw-r-- 1 xocel xocel 1115684232 sep  8 18:42 ./research/dags/old/full-R23-f2e59013a0a37983
-rw-rw-r-- 1 xocel xocel 1124070024 sep  8 18:46 ./research/dags/old/full-R23-582b06447f087674
-rw-rw-r-- 1 xocel xocel 1132461960 sep  8 18:59 ./research/dags/old/full-R23-6d29f6dd1270e497
-rw-rw-r-- 1 xocel xocel 1140849544 sep  8 19:01 ./research/dags/old/full-R23-c307e5620454e771
-rw-rw-r-- 1 xocel xocel 1149232776 sep  8 19:05 ./research/dags/old/full-R23-ec9d541d1c32bec7
```
