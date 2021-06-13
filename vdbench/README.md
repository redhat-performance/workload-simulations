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


<head>
 <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
 <meta name="Author" content="Made by 'tree'">
 <meta name="GENERATOR" content="$Version: $ tree v1.8.0 (c) 1996 - 2018 by Steve Baker, Thomas Moore, Francesc Rocher, Florian Sesser, Kyosuke Tokoro $">
 <title>Directory Tree</title>
 <style type="text/css">
  <!--
  BODY { font-family : ariel, monospace, sans-serif; }
  P { font-weight: normal; font-family : ariel, monospace, sans-serif; color: black; background-color: transparent;}
  B { font-weight: normal; color: black; background-color: transparent;}
  A:visited { font-weight : normal; text-decoration : none; background-color : transparent; margin : 0px 0px 0px 0px; padding : 0px 0px 0px 0px; display: inline; }
  A:link    { font-weight : normal; text-decoration : none; margin : 0px 0px 0px 0px; padding : 0px 0px 0px 0px; display: inline; }
  A:hover   { color : #000000; font-weight : normal; text-decoration : underline; background-color : yellow; margin : 0px 0px 0px 0px; padding : 0px 0px 0px 0px; display: inline; }
  A:active  { color : #000000; font-weight: normal; background-color : transparent; margin : 0px 0px 0px 0px; padding : 0px 0px 0px 0px; display: inline; }
  .VERSION { font-size: small; font-family : arial, sans-serif; }
  .NORM  { color: black;  background-color: transparent;}
  .FIFO  { color: purple; background-color: transparent;}
  .CHAR  { color: yellow; background-color: transparent;}
  .DIR   { color: blue;   background-color: transparent;}
  .BLOCK { color: yellow; background-color: transparent;}
  .LINK  { color: aqua;   background-color: transparent;}
  .SOCK  { color: fuchsia;background-color: transparent;}
  .EXEC  { color: green;  background-color: transparent;}
  -->
 </style>
</head>
<body>

   [vdbench]: <https://www.oracle.com/downloads/server-storage/vdbench-downloads.html>


   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
