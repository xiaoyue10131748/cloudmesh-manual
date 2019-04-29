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
| user             | mallik30                                              |
| version          | #50-Ubuntu SMP Wed Mar 13 10:44:52 UTC 2019           |
| win_version      |                                                       |
+------------------+-------------------------------------------------------+
+---------------------------------+------+--------------------------+--------+-------------+-------------+
| timer                           | time | node                     | system | mac_version | win_version |
+---------------------------------+------+--------------------------+--------+-------------+-------------+
| PUT file                        | 0.41 | ('mallik30-VirtualBox',) | Linux  |             |             |
| GET file                        | 0.18 | ('mallik30-VirtualBox',) | Linux  |             |             |
| LIST Directory                  | 0.44 | ('mallik30-VirtualBox',) | Linux  |             |             |
| CREATE DIR                      | 0.72 | ('mallik30-VirtualBox',) | Linux  |             |             |
| SEARCH file                     | 0.42 | ('mallik30-VirtualBox',) | Linux  |             |             |
| DELETE Directory                | 0.49 | ('mallik30-VirtualBox',) | Linux  |             |             |
| PUT Directory --recursive       | 3.69 | ('mallik30-VirtualBox',) | Linux  |             |             |
| GET Directory --recursive       | 1.78 | ('mallik30-VirtualBox',) | Linux  |             |             |
| DELETE Sub-directory            | 0.79 | ('mallik30-VirtualBox',) | Linux  |             |             |
| LIST Directory --recursive      | 0.5  | ('mallik30-VirtualBox',) | Linux  |             |             |
| LIST Sub-directory --recursive  | 0.5  | ('mallik30-VirtualBox',) | Linux  |             |             |
| SEARCH file --recursive         | 0.49 | ('mallik30-VirtualBox',) | Linux  |             |             |
| SEARCH file under a sub-dir --r | 0.44 | ('mallik30-VirtualBox',) | Linux  |             |             |
| SEARCH file under root dir --r  | 0.48 | ('mallik30-VirtualBox',) | Linux  |             |             |
+---------------------------------+------+--------------------------+--------+-------------+-------------+
```
