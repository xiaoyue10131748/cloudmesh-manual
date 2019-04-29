## Azure Blob Storage

```bash
Internet Speedtest:
ping: 11 ms
download: 129.68 Mbps
upload: 11.73 Mbps
```

Benchmark results for Azure Blob storage under cloudmesh-storage.

```
# ######################################################################
# Benchmark results for 'azureblob' Storage
# ######################################################################

+------------------+-------------------------------------------------------+
| Machine Arribute | Time/s                                                |
+------------------+-------------------------------------------------------+
| mac_version      |                                                       |
| machine          | ('x86_64',)                                           |
| node             | ('mallik30-VirtualBox',)                              |
| platform         | Linux-4.15.0-47-generic-x86_64-with-debian-buster-sid |
| processor        | ('x86_64',)                                           |
| processors       | Linux                                                 |
| python           | 3.7.2 (default, Feb 11 2019, 00:01:16)                |
|                  | [GCC 7.3.0]                                           |
| release          | ('4.15.0-47-generic',)                                |
| sys              | linux                                                 |
| system           | Linux                                                 |
| user             | testuser                                              |
| version          | #50-Ubuntu SMP Wed Mar 13 10:44:52 UTC 2019           |
| win_version      |                                                       |
+------------------+-------------------------------------------------------+
+---------------------------------+------+--------------------------+--------+-------------+-------------+
| timer                           | time | node                     | system | mac_version | win_version |
+---------------------------------+------+--------------------------+--------+-------------+-------------+
| PUT file                        | 0.31 | ('testuser-VirtualBox',) | Linux  |             |             |
| GET file                        | 0.15 | ('testuser-VirtualBox',) | Linux  |             |             |
| LIST Directory                  | 0.37 | ('testuser-VirtualBox',) | Linux  |             |             |
| CREATE DIR                      | 0.53 | ('testuser-VirtualBox',) | Linux  |             |             |
| SEARCH file                     | 0.37 | ('testuser-VirtualBox',) | Linux  |             |             |
| DELETE Directory                | 0.43 | ('testuser-VirtualBox',) | Linux  |             |             |
| PUT Directory --recursive       | 3.57 | ('testuser-VirtualBox',) | Linux  |             |             |
| GET Directory --recursive       | 1.7  | ('testuser-VirtualBox',) | Linux  |             |             |
| DELETE Sub-directory            | 0.76 | ('testuser-VirtualBox',) | Linux  |             |             |
| LIST Directory --recursive      | 0.44 | ('testuser-VirtualBox',) | Linux  |             |             |
| LIST Sub-directory --recursive  | 0.43 | ('testuser-VirtualBox',) | Linux  |             |             |
| SEARCH file --recursive         | 0.32 | ('testuser-VirtualBox',) | Linux  |             |             |
| SEARCH file under a sub-dir --r | 0.39 | ('testuser-VirtualBox',) | Linux  |             |             |
| SEARCH file under root dir --r  | 0.4  | ('testuser-VirtualBox',) | Linux  |             |             |
+---------------------------------+------+--------------------------+--------+-------------+-------------+
```
