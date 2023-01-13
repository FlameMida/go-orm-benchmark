# ORM Benchmark

_(forked from https://github.com/yusaer/orm-benchmark)_

### Environment

-  go1.19 

### PostgreSQL

- PostgreSQL 15 

### ORMs

All package run in no-cache mode.

- [beego/orm](https://github.com/astaxie/beego/tree/master/orm)
- [gorm 2](https://github.com/go-gorm/gorm)
- [pg](https://github.com/go-pg/pg)
- [sqlc](https://github.com/kyleconroy/sqlc) (partially)
- [xorm](https://github.com/xormplus/xorm)

See [`go.mod`](https://github.com/frederikhors/orm-benchmark/blob/master/go.mod) for their latest versions.

### Run

```shell
# all
orm-benchmark -multi=20 -orm=all
# portion
orm-benchmark -multi=20 -orm=gorm
orm-benchmark -multi=20 -orm=pg
orm-benchmark -multi=20 -orm=bun
# ... and so on...
```

### Results

See[`results.md`](https://github.com/FlameMida/go-orm-benchmark/tree/master/results.md)

