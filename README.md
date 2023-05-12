<img src="https://github.com/chdb-io/chdb/raw/pybind/docs/_static/snake-chdb.png" />

## 📦 [chdb package repo](https://chdb-io.github.io)

[![Debian and RPM Repo](https://github.com/chdb-io/chdb-io.github.io/actions/workflows/repo.yml/badge.svg)](https://github.com/chdb-io/chdb-io.github.io/actions/workflows/repo.yml)

This `deb`/`rpm` repository is powered by [Github Actions](https://github.com/chdb-io/chdb.github.io/tree/main/.github), [Github Pages](https://jon.sprig.gs/blog/post/2835) and [nfpm](https://nfpm.goreleaser.com/)

<!-- update: 202305111130 -->

<br>

### Library Installation _(amd64)_

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

<br>
