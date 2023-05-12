---
layout: home
title: chDB
---

<div align="center">
  <img src="docs/_static/snake-chdb.png" height="100">
</div>

[![Build](https://github.com/auxten/chdb/actions/workflows/build_wheels.yml/badge.svg?branch=pybind)](https://github.com/auxten/chdb/actions/workflows/build_wheels.yml)
[![PyPI](https://img.shields.io/pypi/v/chdb.svg)](https://pypi.org/project/chdb/)
[![Monthly Downloads](https://pepy.tech/badge/chdb/month)](https://pepy.tech/project/chdb)
[![Discord](https://img.shields.io/discord/1098133460310294528?logo=Discord)](https://discord.gg/Njw5YXSPPc)
[![Twitter](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&label=Twitter)](https://twitter.com/auxten)

# chDB

> chDB is an embedded SQL OLAP Engine powered by ClickHouse

## Features
     
* In-process SQL OLAP Engine, powered by ClickHouse
* No need to install ClickHouse
* Minimized data copy from C++ to Python with [python memoryview](https://docs.python.org/3/c-api/memoryview.html)
* Input&Output support Parquet, CSV, JSON, Arrow, ORC and 60+[more](https://clickhouse.com/docs/en/interfaces/formats) formats, [samples](tests/format_output.py)

## Usage

### Run in command line
> `python3 -m chdb SQL [OutputFormat]`
```bash
python3 -m chdb "SELECT 1,'abc'" Pretty
```

Currently, chDB only supports `query` function, which is used to execute SQL and return desired format data.

```python
import chdb
res = chdb.query('select version()', 'Pretty'); print(res.data())
```

### Run in library

Experimental `chdb` binding examples: 

* [chdb-go](https://github.com/chdb-io/chdb-go)
* [chdb-node](https://github.com/chdb-io/chdb-node)
* [chdb-bun](https://github.com/chdb-io/chdb-bun)
* [chdb-rust](https://github.com/chdb-io/chdb-rust)

Please install the latest libchdb dynamic library _(amd64 only)_

#### :package: Debian Repository
```
wget -qO- https://chdb-io.github.io/chdb-io.gpg | sudo tee /etc/apt/trusted.gpg.d/chdb-io.gpg >/dev/null
echo "deb [arch=all signed-by=/etc/apt/trusted.gpg.d/chdb-io.gpg] https://chdb-io.github.io/deb stable main" | sudo tee /etc/apt/sources.list.d/chdb-io.list >/dev/null
apt update && apt install libchdb
```

#### :package: RPM Repository
```
wget -qO- https://chdb-io.github.io/chdb-io.repo | sudo tee /etc/yum.repos.d/chdb-io.repo >/dev/null
yum install -y libchdb
```

#### :package: Manual
```
wget https://github.com/metrico/libchdb/releases/latest/download/libchdb.zip
unzip libchdb_amd64.zip
mv libchdb.so /usr/lib/libchdb.so
```
