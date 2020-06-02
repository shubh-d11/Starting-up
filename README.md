# Starting-up
Contains all the details regarding my setup

### OS Information
```
$hostnamectl

   Static hostname: knapsuck
         Icon name: computer-laptop
           Chassis: laptop
        Machine ID: bd6cba6fa357428d8a59234cf7257f0b
           Boot ID: d00efe85699a4dbf8c5f43c2c9aedba3
  Operating System: Ubuntu 20.04 LTS
            Kernel: Linux 5.4.0-33-generic
      Architecture: x86-64

```

### Java Information
```
$java -version

openjdk version "1.8.0_252"
OpenJDK Runtime Environment (build 1.8.0_252-8u252-b09-1ubuntu1-b09)
OpenJDK 64-Bit Server VM (build 25.252-b09, mixed mode)

```

### MySQL Information
```
$status
--------------
mysql  Ver 8.0.20-0ubuntu0.20.04.1 for Linux on x86_64 ((Ubuntu))

Connection id:		15
Current database:
Current user:		root@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		8.0.20-0ubuntu0.20.04.1 (Ubuntu)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	utf8mb4
Db     characterset:	utf8mb4
Client characterset:	utf8mb4
Conn.  characterset:	utf8mb4
UNIX socket:		/var/run/mysqld/mysqld.sock
Binary data as:		Hexadecimal
Uptime:			7 hours 49 min 41 sec

Threads: 2  Questions: 18  Slow queries: 0  Opens: 128  Flush tables: 3  Open tables: 49  Queries per second avg: 0.000
--------------

$show databases

+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| testdb             |
+--------------------+
5 rows in set (0.12 sec)
```

### Redis Information
```
$redis-cli INFO

# Server
redis_version:5.0.7
redis_git_sha1:00000000
redis_git_dirty:0
redis_build_id:636cde3b5c7a3923
redis_mode:standalone
os:Linux 5.4.0-33-generic x86_64
arch_bits:64
multiplexing_api:epoll
atomicvar_api:atomic-builtin
gcc_version:9.2.1
process_id:791214
run_id:60262de859c9ca645626a6292e433a5958222267
tcp_port:6379
uptime_in_seconds:78
uptime_in_days:0
hz:10
configured_hz:10
lru_clock:14053261
executable:/home/cyberpunk/redis-server
config_file:

# Clients
connected_clients:1
client_recent_max_input_buffer:2
client_recent_max_output_buffer:0
blocked_clients:0

# Memory
used_memory:858992
used_memory_human:838.86K
used_memory_rss:7847936
used_memory_rss_human:7.48M
used_memory_peak:858992
used_memory_peak_human:838.86K
used_memory_peak_perc:100.12%
used_memory_overhead:845766
used_memory_startup:796072
used_memory_dataset:13226
used_memory_dataset_perc:21.02%
allocator_allocated:1591624
allocator_active:1925120
allocator_resident:9269248
total_system_memory:8228429824
total_system_memory_human:7.66G
used_memory_lua:41984
used_memory_lua_human:41.00K
used_memory_scripts:0
used_memory_scripts_human:0B
number_of_cached_scripts:0
maxmemory:0
maxmemory_human:0B
maxmemory_policy:noeviction
allocator_frag_ratio:1.21
allocator_frag_bytes:333496
allocator_rss_ratio:4.81
allocator_rss_bytes:7344128
rss_overhead_ratio:0.85
rss_overhead_bytes:-1421312
mem_fragmentation_ratio:9.61
mem_fragmentation_bytes:7030952
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
rdb_last_save_time:1591111487
rdb_last_bgsave_status:ok
rdb_last_bgsave_time_sec:-1
rdb_current_bgsave_time_sec:-1
rdb_last_cow_size:0
aof_enabled:0
aof_rewrite_in_progress:0
aof_rewrite_scheduled:0
aof_last_rewrite_time_sec:-1
aof_current_rewrite_time_sec:-1
aof_last_bgrewrite_status:ok
aof_last_write_status:ok
aof_last_cow_size:0

# Stats
total_connections_received:2
total_commands_processed:2
instantaneous_ops_per_sec:0
total_net_input_bytes:61
total_net_output_bytes:11534
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
latest_fork_usec:0
migrate_cached_sockets:0
slave_expires_tracked_keys:0
active_defrag_hits:0
active_defrag_misses:0
active_defrag_key_hits:0
active_defrag_key_misses:0

# Replication
role:master
connected_slaves:0
master_replid:7337924362bb5b4dc2f300caa1de038088d0e028
master_replid2:0000000000000000000000000000000000000000
master_repl_offset:0
second_repl_offset:-1
repl_backlog_active:0
repl_backlog_size:1048576
repl_backlog_first_byte_offset:0
repl_backlog_histlen:0

# CPU
used_cpu_sys:0.127786
used_cpu_user:0.122872
used_cpu_sys_children:0.000000
used_cpu_user_children:0.000000

# Cluster
cluster_enabled:0

# Keyspace

```
