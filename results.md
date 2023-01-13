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
  raw_stmt:     1.16s      1159720 ns/op     681 B/op     14 allocs/op
 sqlc_prep:     1.18s      1182879 ns/op    2449 B/op     62 allocs/op
 gorm_prep:     1.22s      1217035 ns/op    5439 B/op     69 allocs/op
       raw:     1.23s      1232573 ns/op     829 B/op     14 allocs/op
      sqlc:     1.26s      1256917 ns/op    2588 B/op     62 allocs/op
        pg:     1.26s      1257881 ns/op    2052 B/op     10 allocs/op
      gorm:     1.27s      1273957 ns/op    7350 B/op    109 allocs/op
 beego_orm:     2.01s      2013202 ns/op    2584 B/op     60 allocs/op
      xorm:     2.23s      2232230 ns/op    2975 B/op     79 allocs/op

  1000 times - MultiInsert 100 row
       raw:     1.91s      1912153 ns/op  212157 B/op    640 allocs/op
  raw_stmt:     1.97s      1965942 ns/op  208562 B/op    640 allocs/op
 gorm_prep:     2.35s      2349796 ns/op  255118 B/op   1991 allocs/op
        pg:     2.48s      2479868 ns/op    5419 B/op    112 allocs/op
      gorm:     2.99s      2989048 ns/op  297148 B/op   5433 allocs/op
      xorm:     3.50s      3495253 ns/op  259715 B/op   5815 allocs/op
 beego_orm:     3.64s      3635435 ns/op  189015 B/op   2747 allocs/op
 sqlc_prep:     TBD
      sqlc:     TBD

  1000 times - Update
  raw_stmt:     0.77s       767059 ns/op     728 B/op     15 allocs/op
       raw:     0.78s       775056 ns/op     712 B/op     14 allocs/op
      sqlc:     1.17s      1174019 ns/op     808 B/op     13 allocs/op
        pg:     1.21s      1213889 ns/op     768 B/op      9 allocs/op
 sqlc_prep:     1.23s      1225802 ns/op     824 B/op     14 allocs/op
 gorm_prep:     1.24s      1235438 ns/op    5085 B/op     60 allocs/op
      gorm:     1.30s      1303501 ns/op    6828 B/op    103 allocs/op
      xorm:     2.02s      2021314 ns/op    3042 B/op    110 allocs/op
 beego_orm:     2.17s      2165065 ns/op    1944 B/op     47 allocs/op

  1000 times - Read
      sqlc:     0.78s       779210 ns/op    1808 B/op     55 allocs/op
       raw:     0.79s       785597 ns/op    1716 B/op     54 allocs/op
  raw_stmt:     0.79s       788040 ns/op    1747 B/op     55 allocs/op
        pg:     0.79s       793981 ns/op     876 B/op     20 allocs/op
 sqlc_prep:     0.81s       807388 ns/op    1840 B/op     56 allocs/op
 gorm_prep:     0.81s       808777 ns/op    4470 B/op     89 allocs/op
      gorm:     0.85s       852006 ns/op    4845 B/op    102 allocs/op
 beego_orm:     1.63s      1632831 ns/op    2656 B/op     87 allocs/op
      xorm:     1.66s      1663639 ns/op    9303 B/op    243 allocs/op

  1000 times - MultiRead limit 100
  raw_stmt:     0.95s       945512 ns/op   25519 B/op   1041 allocs/op
       raw:     0.96s       963167 ns/op   25484 B/op   1040 allocs/op
      sqlc:     0.97s       973696 ns/op   60352 B/op   1254 allocs/op
 sqlc_prep:     1.00s      1000534 ns/op   60387 B/op   1255 allocs/op
        pg:     1.00s      1000853 ns/op   22297 B/op    629 allocs/op
 gorm_prep:     1.18s      1176960 ns/op   43371 B/op   2082 allocs/op
      gorm:     1.23s      1231849 ns/op   45273 B/op   2384 allocs/op
 beego_orm:     2.60s      2604368 ns/op   55857 B/op   3089 allocs/op
      xorm:     doesn't work
```

- orm-benchmark -multi=20

```
  
  4000 times - Insert
  raw_stmt:     4.55s      1137120 ns/op     674 B/op     14 allocs/op
       raw:     4.64s      1160355 ns/op     700 B/op     13 allocs/op
        pg:     4.79s      1197197 ns/op    1372 B/op     10 allocs/op
 gorm_prep:     4.80s      1199313 ns/op    5273 B/op     68 allocs/op
 sqlc_prep:     4.80s      1201012 ns/op    2451 B/op     62 allocs/op
      sqlc:     4.85s      1211589 ns/op    2462 B/op     62 allocs/op
      gorm:     4.92s      1229011 ns/op    7261 B/op    110 allocs/op
      xorm:     7.77s      1942910 ns/op    2953 B/op     79 allocs/op
 beego_orm:     7.85s      1963090 ns/op    2586 B/op     60 allocs/op

  4000 times - MultiInsert 100 row
  raw_stmt:     7.26s      1814182 ns/op  207798 B/op    639 allocs/op
       raw:     7.38s      1844865 ns/op  212204 B/op    639 allocs/op
 gorm_prep:     8.11s      2027930 ns/op  255399 B/op   1991 allocs/op
        pg:     9.43s      2356270 ns/op    3844 B/op    112 allocs/op
      gorm:    10.07s      2517503 ns/op  296301 B/op   5433 allocs/op
      xorm:    13.26s      3315622 ns/op  259733 B/op   5815 allocs/op
 beego_orm:    13.53s      3382039 ns/op  189099 B/op   2747 allocs/op
      sqlc:     TBD
 sqlc_prep:     TBD

  4000 times - Update
       raw:     3.01s       752238 ns/op     712 B/op     14 allocs/op
  raw_stmt:     3.02s       755264 ns/op     728 B/op     15 allocs/op
 gorm_prep:     4.67s      1166395 ns/op    5085 B/op     60 allocs/op
      sqlc:     4.74s      1184730 ns/op     808 B/op     13 allocs/op
 sqlc_prep:     4.80s      1199998 ns/op     824 B/op     14 allocs/op
        pg:     4.84s      1209169 ns/op     770 B/op      9 allocs/op
      gorm:     4.93s      1231347 ns/op    6830 B/op    103 allocs/op
      xorm:     7.82s      1955609 ns/op    3042 B/op    110 allocs/op
 beego_orm:     7.92s      1979031 ns/op    1945 B/op     47 allocs/op

  4000 times - Read
      sqlc:     3.02s       755076 ns/op    1809 B/op     55 allocs/op
 sqlc_prep:     3.04s       759197 ns/op    1841 B/op     56 allocs/op
  raw_stmt:     3.04s       760319 ns/op    1746 B/op     55 allocs/op
       raw:     3.05s       762459 ns/op    1714 B/op     54 allocs/op
 gorm_prep:     3.11s       777223 ns/op    4471 B/op     89 allocs/op
        pg:     3.12s       780957 ns/op     874 B/op     20 allocs/op
      gorm:     3.31s       827199 ns/op    4843 B/op    102 allocs/op
 beego_orm:     6.17s      1543128 ns/op    2658 B/op     87 allocs/op
      xorm:     6.40s      1600883 ns/op    9304 B/op    243 allocs/op

  4000 times - MultiRead limit 100
       raw:     3.70s       923830 ns/op   25487 B/op   1040 allocs/op
  raw_stmt:     3.75s       937243 ns/op   25516 B/op   1041 allocs/op
      sqlc:     3.86s       965492 ns/op   60347 B/op   1254 allocs/op
 sqlc_prep:     3.86s       965794 ns/op   60389 B/op   1255 allocs/op
        pg:     4.03s      1007860 ns/op   24470 B/op    629 allocs/op
 gorm_prep:     4.54s      1134146 ns/op   43388 B/op   2082 allocs/op
      gorm:     4.76s      1189120 ns/op   45239 B/op   2384 allocs/op
 beego_orm:     7.55s      1888438 ns/op   55866 B/op   3089 allocs/op
      xorm:     doesn't work
```
