# redis-with-sentinel
This configuration is for setting up redis with sentinel.  
You need at least 3 server as stated in the manual.  
Please note that, I'm using redis only for cache.

## Install redis-server
```
sudo apt install redis-server
```
After installing redis-server, you can find redis.conf in /etc/redis/redis.conf  
It is a good practice to backup the original conf. After that just edit redis.conf according the sample in this git.  
If you plan to setup master-replica with sentinel, you need to create at least 3 servers.  
Repeat the process for other servers, just don't forget to define different ip address for each server.  
e.g:  
redis-master = 192.168.1.30  
redis-replica1 = 192.168.1.31  
redis-replica2 = 192.168.1.32

## Install redis-sentinel
```
sudo apt install redis-sentinel
```
After installing redis-sentinel, you can find sentinel.conf in /etc/redis/sentinel.conf  
It is a good practice to backup the original conf. After that just edit sentinel.conf according the sample in this git.  
You need to install redis-sentinel to all server you created.
