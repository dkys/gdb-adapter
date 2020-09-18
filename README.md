gdb adapter [![Build Status](https://travis-ci.org/vance-liu/gdb-adapter.svg?branch=master)](https://travis-ci.org/vance-liu/gdb-adapter) [![Coverage Status](https://coveralls.io/repos/github/vance-liu/gdb-adapter/badge.svg?branch=master)](https://coveralls.io/github/vance-liu/gdb-adapter?branch=master) [![Godoc](https://godoc.org/github.com/vance-liu/gdb-adapter?status.svg)](https://godoc.org/github.com/vance-liu/gdb-adapter)
====

[GF ORM](https://github.com/gogf/gf) adapter for [Casbin](https://github.com/casbin/casbin). 

Based on [GF ORM](https://github.com/gogf/gf), and tested in:
- MySQL
- PostgreSQL

## Installation

    go get gitee.com/yxmmer/gdb-adapter

## Usage example

```go
opts := &Adapter{
    DriverName: "mysql",
    DataSourceName: "root:1234@tcp(127.0.0.1:3306)/casbin",
    TableName: "casbin_rule",
    // or reuse an existing connection:
    // db: yourDBConn,
}

a := NewAdapterFromOptions(opts)
e := casbin.NewEnforcer("examples/rbac_model.conf", a)
```

## Notice
you should create the database on your own.

## Getting Help

- [Casbin](https://github.com/casbin/casbin)

## License

This project is under Apache 2.0 License. See the [LICENSE](LICENSE) file for the full license text.
