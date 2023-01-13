# Results

- orm-benchmark (with no flags)

```
   200 times - Insert
  raw_stmt:     0.23s      1129138 ns/op     718 B/op     14 allocs/op
       raw:     0.23s      1169738 ns/op    1496 B/op     18 allocs/op
 sqlc_prep:     0.23s      1173255 ns/op    2460 B/op     61 allocs/op
        pg:     0.24s      1213889 ns/op    7083 B/op     11 allocs/op
      sqlc:     0.24s      1224051 ns/op    3273 B/op     66 allocs/op
 gorm_prep:     0.25s      1227385 ns/op    6289 B/op     72 allocs/op
      gorm:     0.25s      1232124 ns/op    7891 B/op    110 allocs/op
      xorm:     0.39s      1946119 ns/op    3082 B/op     80 allocs/op
 beego_orm:     0.40s      2004038 ns/op    2589 B/op     60 allocs/op

   200 times - MultiInsert 100 row
  raw_stmt:     0.36s      1793209 ns/op  208911 B/op    646 allocs/op
       raw:     0.36s      1806882 ns/op  214193 B/op    646 allocs/op
        pg:     0.47s      2360166 ns/op    8578 B/op    112 allocs/op
 gorm_prep:     0.49s      2443002 ns/op  255449 B/op   1990 allocs/op
      gorm:     0.51s      2559697 ns/op  295435 B/op   5432 allocs/op
      xorm:     0.66s      3303655 ns/op  259833 B/op   5816 allocs/op
 beego_orm:     0.71s      3565982 ns/op  189147 B/op   2747 allocs/op
 sqlc_prep:     TBD
      sqlc:     TBD

   200 times - Update
  raw_stmt:     0.15s       749615 ns/op     730 B/op     15 allocs/op
       raw:     0.15s       755483 ns/op     714 B/op     14 allocs/op
 sqlc_prep:     0.23s      1157213 ns/op     824 B/op     14 allocs/op
      sqlc:     0.23s      1159561 ns/op     810 B/op     13 allocs/op
 gorm_prep:     0.23s      1166867 ns/op    5095 B/op     60 allocs/op
        pg:     0.24s      1193237 ns/op     768 B/op      9 allocs/op
      gorm:     0.25s      1231640 ns/op    6824 B/op    103 allocs/op
 beego_orm:     0.40s      1984113 ns/op    1947 B/op     47 allocs/op
      xorm:     0.41s      2051797 ns/op    3040 B/op    110 allocs/op

   200 times - Read
 sqlc_prep:     0.15s       750069 ns/op    1840 B/op     56 allocs/op
      sqlc:     0.15s       758024 ns/op    1810 B/op     55 allocs/op
  raw_stmt:     0.15s       766896 ns/op    1760 B/op     55 allocs/op
       raw:     0.15s       774634 ns/op    1733 B/op     54 allocs/op
 gorm_prep:     0.16s       775056 ns/op    4508 B/op     89 allocs/op
        pg:     0.16s       802909 ns/op     873 B/op     20 allocs/op
      gorm:     0.17s       854403 ns/op    4869 B/op    102 allocs/op
 beego_orm:     0.31s      1537275 ns/op    2656 B/op     87 allocs/op
      xorm:     0.32s      1622372 ns/op    9296 B/op    243 allocs/op

   200 times - MultiRead limit 100
  raw_stmt:     0.18s       918233 ns/op   25523 B/op   1041 allocs/op
       raw:     0.19s       951866 ns/op   25479 B/op   1040 allocs/op
 sqlc_prep:     0.19s       967271 ns/op   60373 B/op   1255 allocs/op
      sqlc:     0.19s       972969 ns/op   60347 B/op   1254 allocs/op
        pg:     0.20s       994286 ns/op   22299 B/op    629 allocs/op
 gorm_prep:     0.23s      1150203 ns/op   43387 B/op   2082 allocs/op
      gorm:     0.24s      1202604 ns/op   45256 B/op   2384 allocs/op
 beego_orm:     0.38s      1907212 ns/op   55862 B/op   3089 allocs/op
      xorm:     doesn't work
```

- orm-benchmark -multi=5

```
  1000 times - Insert
  raw_stmt:     1.88s      1876992 ns/op     713 B/op     14 allocs/op
      sqlc:     1.89s      1893039 ns/op    2951 B/op     62 allocs/op
       bun:     1.95s      1946642 ns/op     973 B/op     12 allocs/op
 sqlc_prep:     1.96s      1959731 ns/op    2915 B/op     62 allocs/op
        pg:     1.97s      1972887 ns/op    2172 B/op     12 allocs/op
 beego_orm:     1.97s      1974838 ns/op    2407 B/op     56 allocs/op
       raw:     1.99s      1989314 ns/op     765 B/op     13 allocs/op
      gorm:     2.00s      2002163 ns/op    6691 B/op     87 allocs/op
 gorm_prep:     2.19s      2193652 ns/op    5093 B/op     65 allocs/op
      xorm:     2.66s      2655665 ns/op    3122 B/op     94 allocs/op

  1000 times - MultiInsert 100 row
       raw:     5.10s      5104897 ns/op  135377 B/op    917 allocs/op
  raw_stmt:     5.27s      5265910 ns/op  131303 B/op    917 allocs/op
 beego_orm:     5.46s      5455346 ns/op  179683 B/op   2746 allocs/op
       bun:     5.73s      5728978 ns/op    4288 B/op    214 allocs/op
        pg:     6.15s      6148537 ns/op    5619 B/op    114 allocs/op
 gorm_prep:     6.27s      6266789 ns/op  200131 B/op   2167 allocs/op
      gorm:     7.00s      6996598 ns/op  293820 B/op   3728 allocs/op
      xorm:     9.65s      9652630 ns/op  285790 B/op   7422 allocs/op
      sqlc:     TBD
 sqlc_prep:     TBD

  1000 times - Update
  raw_stmt:     0.66s       656289 ns/op     795 B/op     14 allocs/op
       raw:     0.67s       673473 ns/op     779 B/op     13 allocs/op
      sqlc:     1.86s      1855891 ns/op     881 B/op     14 allocs/op
       bun:     1.90s      1901312 ns/op     588 B/op      4 allocs/op
        pg:     1.95s      1949913 ns/op    1946 B/op     11 allocs/op
 beego_orm:     1.96s      1955216 ns/op    1802 B/op     47 allocs/op
      gorm:     1.96s      1963761 ns/op    6600 B/op     81 allocs/op
 gorm_prep:     2.08s      2079962 ns/op    5139 B/op     59 allocs/op
      xorm:     2.57s      2566849 ns/op    2994 B/op    119 allocs/op
 sqlc_prep:     4.31s      4306308 ns/op     896 B/op     15 allocs/op

  1000 times - Read
 sqlc_prep:     0.66s       662826 ns/op    2230 B/op     52 allocs/op
      sqlc:     0.67s       668075 ns/op    2198 B/op     51 allocs/op
       raw:     0.67s       668364 ns/op    2080 B/op     49 allocs/op
  raw_stmt:     0.67s       668732 ns/op    2111 B/op     50 allocs/op
 gorm_prep:     0.69s       689280 ns/op    4904 B/op     97 allocs/op
       bun:     0.70s       700091 ns/op    1313 B/op     18 allocs/op
        pg:     0.71s       709185 ns/op    1002 B/op     22 allocs/op
 beego_orm:     0.72s       719784 ns/op    2105 B/op     75 allocs/op
      gorm:     0.73s       731898 ns/op    5238 B/op    108 allocs/op
      xorm:     1.42s      1420066 ns/op    8319 B/op    237 allocs/op

  1000 times - MultiRead limit 100
  raw_stmt:     0.89s       889895 ns/op   38396 B/op   1038 allocs/op
       raw:     0.90s       899328 ns/op   38365 B/op   1037 allocs/op
 sqlc_prep:     0.92s       924715 ns/op   73212 B/op   1251 allocs/op
      sqlc:     0.93s       930699 ns/op   73181 B/op   1250 allocs/op
       bun:     1.02s      1024110 ns/op   28800 B/op   1116 allocs/op
        pg:     1.05s      1054427 ns/op   25554 B/op    631 allocs/op
 beego_orm:     1.11s      1107688 ns/op   55245 B/op   3077 allocs/op
 gorm_prep:     1.23s      1233602 ns/op   71245 B/op   3577 allocs/op
      gorm:     1.29s      1285833 ns/op   71642 B/op   3877 allocs/op
      xorm:     doesn't work
```

- orm-benchmark -multi=20

```
  4000 times - Insert
  raw_stmt:     7.49s      1872449 ns/op     718 B/op     14 allocs/op
       raw:     7.50s      1875044 ns/op     727 B/op     13 allocs/op
 beego_orm:     7.56s      1890294 ns/op    2410 B/op     56 allocs/op
      sqlc:     7.61s      1902785 ns/op    2902 B/op     62 allocs/op
 sqlc_prep:     7.68s      1921107 ns/op    2917 B/op     62 allocs/op
       bun:     7.69s      1923437 ns/op     918 B/op     13 allocs/op
 gorm_prep:     7.71s      1927455 ns/op    4985 B/op     65 allocs/op
        pg:     7.88s      1968902 ns/op    1778 B/op     12 allocs/op
      gorm:     8.64s      2159774 ns/op    6676 B/op     88 allocs/op
      xorm:    10.36s      2591181 ns/op    3050 B/op     94 allocs/op

  4000 times - MultiInsert 100 row
  raw_stmt:    19.46s      4865525 ns/op  131076 B/op    916 allocs/op
       raw:    20.01s      5002064 ns/op  135155 B/op    916 allocs/op
 gorm_prep:    23.39s      5848246 ns/op  200057 B/op   2168 allocs/op
       bun:    23.85s      5963499 ns/op    4259 B/op    214 allocs/op
        pg:    23.88s      5970434 ns/op    3986 B/op    114 allocs/op
 beego_orm:    23.90s      5975433 ns/op  179815 B/op   2746 allocs/op
      gorm:    28.97s      7242372 ns/op  293955 B/op   3729 allocs/op
      xorm:    35.60s      8900321 ns/op  286030 B/op   7422 allocs/op
 sqlc_prep:     TBD
      sqlc:     TBD

  4000 times - Update
  raw_stmt:     2.62s       656011 ns/op     773 B/op     14 allocs/op
       raw:     2.63s       656770 ns/op     757 B/op     13 allocs/op
 sqlc_prep:     7.46s      1864336 ns/op     894 B/op     15 allocs/op
 beego_orm:     7.50s      1874009 ns/op    1801 B/op     47 allocs/op
      sqlc:     7.52s      1879374 ns/op     876 B/op     14 allocs/op
 gorm_prep:     7.60s      1900330 ns/op    5123 B/op     59 allocs/op
       bun:     7.68s      1920855 ns/op     591 B/op      4 allocs/op
      gorm:     7.82s      1954842 ns/op    6604 B/op     81 allocs/op
        pg:     8.09s      2022080 ns/op     896 B/op     11 allocs/op
      xorm:    10.27s      2566399 ns/op    2994 B/op    119 allocs/op

  4000 times - Read
 beego_orm:     2.64s       658829 ns/op    2105 B/op     75 allocs/op
      sqlc:     2.64s       659501 ns/op    2190 B/op     51 allocs/op
 sqlc_prep:     2.65s       662342 ns/op    2222 B/op     52 allocs/op
       raw:     2.65s       662669 ns/op    2080 B/op     49 allocs/op
  raw_stmt:     2.69s       672677 ns/op    2112 B/op     50 allocs/op
 gorm_prep:     2.75s       686810 ns/op    4908 B/op     97 allocs/op
       bun:     2.76s       689577 ns/op    1313 B/op     18 allocs/op
        pg:     2.84s       710984 ns/op    1000 B/op     22 allocs/op
      gorm:     2.91s       726527 ns/op    5240 B/op    108 allocs/op
      xorm:     5.69s      1423129 ns/op    8322 B/op    237 allocs/op

  4000 times - MultiRead limit 100
       raw:     3.56s       889343 ns/op   38356 B/op   1037 allocs/op
  raw_stmt:     3.57s       891465 ns/op   38388 B/op   1038 allocs/op
      sqlc:     3.72s       930181 ns/op   73176 B/op   1250 allocs/op
 sqlc_prep:     3.73s       933592 ns/op   73208 B/op   1251 allocs/op
        pg:     3.93s       981776 ns/op   24532 B/op    631 allocs/op
       bun:     4.07s      1016640 ns/op   28858 B/op   1116 allocs/op
 beego_orm:     4.19s      1048494 ns/op   55253 B/op   3077 allocs/op
 gorm_prep:     4.96s      1240677 ns/op   71236 B/op   3577 allocs/op
      gorm:     5.19s      1297135 ns/op   71628 B/op   3877 allocs/op
      xorm:     doesn't work
```
