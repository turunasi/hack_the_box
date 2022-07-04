# Redeemer
## task 1
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# nmap -sV -p-10000 -T4 <your target ip>
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-04 04:57 UTC
Nmap scan report for <your target ip>
Host is up (0.20s latency).
Not shown: 9899 closed tcp ports (reset), 100 filtered tcp ports (no-response)
PORT     STATE SERVICE VERSION
6379/tcp open  redis   Redis key-value store 5.0.7

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 235.12 seconds
```
6379
## task 2
redis
## task 3
In-memory Database
## task 4
```
apt-get install redis
```
redis-cli
## task 5
```
redis-cli -h <your target ip>
```
## task 6
```
info
```
## task 7
5.0.7
## task 8
```
select
```
## task 9
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# redis-cli -h <your target ip>

<your target ip>:6379> info
# Server
redis_version:5.0.7
redis_git_sha1:00000000
redis_git_dirty:0
redis_build_id:66bd629f924ac924
redis_mode:standalone
os:Linux 5.4.0-77-generic x86_64
arch_bits:64
multiplexing_api:epoll
atomicvar_api:atomic-builtin
gcc_version:9.3.0
process_id:752
run_id:9b25178dbe0496212724bbd179b4b67b6d24102f
tcp_port:6379
uptime_in_seconds:4736
uptime_in_days:0
hz:10
configured_hz:10
lru_clock:12745512
executable:/usr/bin/redis-server
config_file:/etc/redis/redis.conf

# Clients
connected_clients:1
client_recent_max_input_buffer:2
client_recent_max_output_buffer:0
blocked_clients:0

# Memory
used_memory:859624
used_memory_human:839.48K
used_memory_rss:5992448
used_memory_rss_human:5.71M
used_memory_peak:859624
used_memory_peak_human:839.48K
used_memory_peak_perc:100.00%
used_memory_overhead:846142
used_memory_startup:796224
used_memory_dataset:13482
used_memory_dataset_perc:21.26%
allocator_allocated:1514936
allocator_active:1875968
allocator_resident:9134080
total_system_memory:2084024320
total_system_memory_human:1.94G
used_memory_lua:41984
used_memory_lua_human:41.00K
used_memory_scripts:0
used_memory_scripts_human:0B
number_of_cached_scripts:0
maxmemory:0
maxmemory_human:0B
maxmemory_policy:noeviction
allocator_frag_ratio:1.24
allocator_frag_bytes:361032
allocator_rss_ratio:4.87
allocator_rss_bytes:7258112
rss_overhead_ratio:0.66
rss_overhead_bytes:-3141632
mem_fragmentation_ratio:7.33
mem_fragmentation_bytes:5174832
mem_not_counted_for_evict:0
mem_replication_backlog:0
mem_clients_slaves:0
mem_clients_normal:49694
mem_aof_buffer:0
mem_allocator:jemalloc-5.2.1
active_defrag_running:0
lazyfree_pending_objects:0

# Persistence
loading:0
rdb_changes_since_last_save:0
rdb_bgsave_in_progress:0
rdb_last_save_time:1656908845
rdb_last_bgsave_status:ok
rdb_last_bgsave_time_sec:0
rdb_current_bgsave_time_sec:-1
rdb_last_cow_size:413696
aof_enabled:0
aof_rewrite_in_progress:0
aof_rewrite_scheduled:0
aof_last_rewrite_time_sec:-1
aof_current_rewrite_time_sec:-1
aof_last_bgrewrite_status:ok
aof_last_write_status:ok
aof_last_cow_size:0

# Stats
total_connections_received:6
total_commands_processed:6
instantaneous_ops_per_sec:0
total_net_input_bytes:293
total_net_output_bytes:14786
instantaneous_input_kbps:0.00
instantaneous_output_kbps:0.00
rejected_connections:0
sync_full:0
sync_partial_ok:0
sync_partial_err:0
expired_keys:0
expired_stale_perc:0.00
expired_time_cap_reached_count:0
evicted_keys:0
keyspace_hits:0
keyspace_misses:0
pubsub_channels:0
pubsub_patterns:0
latest_fork_usec:762
migrate_cached_sockets:0
slave_expires_tracked_keys:0
active_defrag_hits:0
active_defrag_misses:0
active_defrag_key_hits:0
active_defrag_key_misses:0

# Replication
role:master
connected_slaves:0
master_replid:61bcdd4ed182cceedb7bf69fc0415598cebf6035
master_replid2:0000000000000000000000000000000000000000
master_repl_offset:0
second_repl_offset:-1
repl_backlog_active:0
repl_backlog_size:1048576
repl_backlog_first_byte_offset:0
repl_backlog_histlen:0

# CPU
used_cpu_sys:4.373217
used_cpu_user:4.757723
used_cpu_sys_children:0.003357
used_cpu_user_children:0.000000

# Cluster
cluster_enabled:0

# Keyspace
db0:keys=4,expires=0,avg_ttl=0
```
4
## task 10
```
keys *
```
## Submit Flag
```
<your target ip>:6379> select 0
OK
<your target ip>:6379> keys *
1) "stor"
2) "numb"
3) "temp"
4) "flag"
<your target ip>:6379> get flag
```