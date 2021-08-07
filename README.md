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
redis-server [path:config_file]
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

##### String

String are basic operation used to write and read from redis.

* set [key] [value] : sets a value to the key
* get [key] : get the value for the key
* del [key] : deletes the key.
* expire [key] PX|EX  : auto expire the keys
* persist [key] : stop key from auto expire
* mset [key] [value] ... [key] [value] : sets multiple keys and values
* mget [key] ... [key] : gets  values from multiple keys
* exist [key] : check if the given key exist or not 1 -] yes 0 -] No
* incr [key] : increments value associated with the key by 1




* List
* Hashes
* Set








#### Redis Transaction

* Multi
* Exec
* Discard
* Watch
* Unwatch




