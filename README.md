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

##### String Operations

* set [key] [value] : sets a value to the key
* get [key] : get the value for the key
* del [key] : deletes the key.
* expire [key] PX|EX  : auto expire the keys
* persist [key] : stop key from auto expire
* mset [key] [value] ... [key] [value] : sets multiple keys and values
* mget [key] ... [key] : gets  values from multiple keys
* exist [key] : check if the given key exist or not 1 -] yes 0 -] No
* incr [key] : increments value associated with the key by 1

#### List

List is used to store multiple values for a single key.

##### List Operations

* lpush [key] [value] ... [value] : sets values for the key from the left of the list.
* rpush [key] [value] ... [value] : sets values for the key from the right of the list.
* lrange [key] [start] [end]  : get values from the key by the start and end index. 
(Note : -1 is used to indicate the end of the list)
* llen [key]  : get the length of the list.
* lpop [key] : remove the first elemet from the list at the left.
* rpop [key] : remove the first element from the list at the right.
* ltrim [key] [start] [end] : remove all the values except the range specified in the list.

#### Hashes

A Hashes is a  group of keys & values.

##### Hash Operations

* hset [key] [field] [value]   : stores a field and value to the key.
* hget [key] [field] [field] : gets the values for the field from the key.
* hmset [key] [field] [value] ... [field] [value] : stores multiple field and value to the key.
* hmget [key] [field] [value] ... [field] [value] : get multiple field and value from the key.

#### Set

Set is also a list with difference in unique value persistence.
 
##### Set Operations

* sadd [key] [value] : adds values to the set.
* smembers [key] : gets values from the set.
* sismember [key] [value] : check if the member exist in set.
* scard [key] : get the total number.
* sdiff [set1] [set2]  : list the diffference between the sets.
* sdiffstore [setA] [set1] [set2] : store the difference between set1 and set2 inside setA.
* spop [key] : remove the element from the set.
* srem [key] [obj] : remove the value from the set.


#### Redis Transaction

Redis transaction offer ACID property of a database.

##### Transaction Type

* Multi : starts a transaction
* Exec : executes a transaction
* Discard : discard the existing transcation
* Watch : watch a variable , if the variable encounters a change then the redis transaction will fail.
* Unwatch : unwatch will remvoe the watch operation of the variable.




