# Workload simulations patterns -  _using vdbench_  .
```
In this document I will share a few applications workload I modeled and the 
VDbench configuration files I used in order to run them as a benchmark.
```

## Short disclaimer
```
Note that in my modeling I only used the main block sizes that were used:
meaning:
For OLTP1 I used 5 different streams of the 4KB block , but in fact when
profiling workload such as OLTP1 you will see that there a lot more block
sizes such as 8,16,28,64,120,512 KB and also fractions of blocks such 
as 0.2,0.44,0.68kb , etc but the occurrence of those blocks is inconsistent 
and extremely varied so in order to get repeatable consistent results I'm only 
using the main blocks in play, that also applies to any other application pattern on the table above.
The block sizes I decided to use are the majority of the workload for example :
in OLTP1 4KB operations accounted  for ~ 90% of the workload in total.
Real applications will might also be compressible & dedupable by x amount which 
will also affect your performance, if you use any of those algorithms.
but that's a completely different topic. 
I will just point out that VDbench supports compressible & dedupable data generation.
```

## How to use 
You will need to aquire the VDbench tool from [vdbench] and run as follows on Windows or Linux respectively :

```
./vdbench.bat -f test_configuration_file

or:

./vdbench.sh -f test_configuration_file


Do not forget to modify the path at which your workload will be generated.
```

## Directory tree

```
    .
    ├── app_patterns
    │   └── excel_fs.vdb
    ├── dbs_patterns
    │   ├── fs
    │   │   ├── odss128_fs.vdb
    │   │   ├── odss2_fs.vdb
    │   │   ├── oltp1_fs.vdb
    │   │   ├── oltp2_fs.vdb
    │   │   └── oltphw_fs.vdb
    │   └── raw
    │       ├── odss128_raw.vdb
    │       ├── odss2_raw.vdb
    │       ├── oltp1_raw.vdb
    │       ├── oltp2_raw.vdb
    │       └── oltphw_raw.vdb
    └── generic_tests
        ├── generic.vdb
        └── mixed.vdb
```

   [vdbench]: <https://www.oracle.com/downloads/server-storage/vdbench-downloads.html>
