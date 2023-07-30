<a href="https://chdb.fly.dev" target="_blank">
  <img src="https://github.com/chdb-io/chdb/raw/pybind/docs/_static/snake-chdb.png" height=150 />
</a>

> chDB is an embedded SQL OLAP Engine powered by ClickHouse

<br>

## chDB

#### Python
```
pip install chdb --upgrade
```

<br>

## libchDB

#### Packages
Install `libchdb` on any `deb` or `rpm` based operating system:

##### :package: Debian Repository
```bash
sudo bash -c 'curl -s https://packagecloud.io/install/repositories/auxten/chdb/script.deb.sh | os=any dist=any bash'
sudo apt install libchdb
```

##### :package: RPM Repository
```bash
sudo bash -c 'curl -s https://packagecloud.io/install/repositories/auxten/chdb/script.rpm.sh | os=rpm_any dist=rpm_any bash'
sudo yum install -y libchdb
```


<br>



### :package: Installation
Install `libchdb` manually on `x64` or `arm64` Linux platforms:


#### Linux
##### x86_64
```bash
wget https://github.com/metrico/libchdb/releases/latest/download/libchdb.zip
unzip libchdb.zip
mv libchdb.so /usr/lib/libchdb.so
```
##### arm64
```bash
wget https://github.com/metrico/libchdb/releases/latest/download/libchdb_arm64.zip
unzip libchdb_arm64.zip
mv libchdb.so /usr/lib/libchdb.so
```
<br>

