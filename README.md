# Redis

 Redis is one of the fastest DB because it does all execution via in-memory.

#### Installation

* Mac 

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

#### Start Redis

starting redis server

```sh
redis-server <path:config_file>
```
#### Stop Redis

stopping redis server

```sh
redis-cli
```
```sh
shutdown
```
#### Redis Benchmarking

This is used to evaluate the performance of redis.

redis-benchmark 

* -h : host ip address
* -p : host port 
* -n : number of request
* -d : payload size (in bytes)
* -t : type of operation

```sh
redis-benchmark -h 127.0.01 -p 6370 -n 1000 -d 10 -t get set
```
#### Redis DataTypes

* String
* List
* Hashes
* Set



#### Redis Transaction
* Multi
* Exec
* Discard
* Watch
* Unwatch




