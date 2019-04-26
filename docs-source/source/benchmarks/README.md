# Benchmarks

Put your penchmarks in separate files into this directory.

## Azure Blob Storage

Benchmark results for Azure Blob storage using cloudmesh-storage.

```bash
# ######################################################################
# Benchmark results for AzureBlob Storage
# ######################################################################

+------------------+-------------------------------------------------------+
| Machine Arribute | Time/s                                                |
+------------------+-------------------------------------------------------+
| mac_version      |                                                       |
| machine          | x86_64                                                |
| node             | testuser-VirtualBox                                   |
| platform         | Linux-4.15.0-47-generic-x86_64-with-debian-buster-sid |
| processor        | x86_64                                                |
| processors       | Linux                                                 |
| release          | 4.15.0-47-generic                                     |
| sys              | linux                                                 |
| system           | Linux                                                 |
| user             | testuser                                              |
| version          | #50-Ubuntu SMP Wed Mar 13 10:44:52 UTC 2019           |
| win_version      | ('', '', '', '')                                      |
+------------------+-------------------------------------------------------+
+---------------------------------+------+---------------------+--------+-------------+------------------+
| timer                           | time | node                | system | mac_version | win_version      |
+---------------------------------+------+---------------------+--------+-------------+------------------+
| PUT file                        | 0.35 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| GET file                        | 0.15 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| LIST Directory                  | 0.42 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| CREATE DIR                      | 0.58 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| SEARCH file                     | 0.41 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| DELETE Directory                | 0.52 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| PUT Directory --recursive       | 3.55 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| GET Directory --recursive       | 1.73 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| DELETE Sub-directory            | 0.82 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| LIST Directory --recursive      | 0.51 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| LIST Sub-directory --recursive  | 0.5  | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| SEARCH file --recursive         | 0.45 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| SEARCH file under a sub-dir --r | 0.45 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
| SEARCH file under root dir --r  | 0.45 | testuser-VirtualBox | Linux  |             | ('', '', '', '') |
+---------------------------------+------+---------------------+--------+-------------+------------------+
```
