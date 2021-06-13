# Software design patterns -  _using vdbench_  .

## Short Disclaimer
Note that in my modeling I only used the main block sizes that were used:
E.g For OLTP1 I used 5 different streams of the 4KB block , but in fact when profiling workload such as OLTP1  you will see that there a lot more block sizes such as 8,16,28,64,120,512 KB and also fractions of blocks such as 0.2,0.44,0.68, KB etc
but the occurrence of those blocks is inconsistent and extremely varied so in order to get repeatable consistent results I'm only using the main blocks in play, that also applies to any other application pattern on the table above.
The block sizes I decided  to use are the majority of the workload for example :
in OLTP1 4KB operations accounted  for ~ 90% of the workload in total.
Real applications will also be compressible & dedupable by x amount which will also affect your performance, if you use any of those, but that's a completely different topic. 
I will just point out that VDbench supports compressible & dedupable data generation.


## How to use 
well , you will need to aquire the vdbcnech tool from [vdbench] and run like so:
```sh
./vdbench.bat -f xxxxx
```
or:
```sh
./vdbench.sh -f xxxxx
```


   [vdbench]: <https://www.oracle.com/downloads/server-storage/vdbench-downloads.html>


   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
