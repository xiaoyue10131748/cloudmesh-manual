## AWS S3 File Storage

Benchmark results for AWS S3 File storage under cloudmesh-storage.

 PING ms : 3
 DOWNLOAD Mbps : 46.86
 UPLOAD Mbps : 35.13

```
+------------------+----------------------------------------------------+
| Machine Arribute | Time/s                                             |
+------------------+----------------------------------------------------+
| mac_version      |                                                    |
| machine          | AMD64                                              |
| node             | DESKTOP-CNS55VM                                    |
| platform         | Windows-10-10.0.17134-SP0                          |
| processor        | Intel64 Family 6 Model 78 Stepping 3, GenuineIntel |
| processors       | Windows                                            |
| release          | 10                                                 |
| sys              | win32                                              |
| system           | Windows                                            |
| version          | 10.0.17134                                         |
| win_version      | ('10', '10.0.17134', 'SP0', 'Multiprocessor Free') |
+------------------+----------------------------------------------------+
+--------------------+------+-----------------+---------+-------------+------------------------------------------+
| timer              | time | node            | system  | mac_version | win_version                              |
+--------------------+------+-----------------+---------+-------------+------------------------------------------+
| awss3 setup        | 0.02 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 create dir 1 | 0.38 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 create dir 2 | 0.22 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 put          | 0.26 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 get          | 0.47 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 list         | 0.77 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 search       | 0.45 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 delete       | 3.41 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                    |      |                 |         |             | 'Multiprocessor Free')                   |
+--------------------+------+-----------------+---------+-------------+------------------------------------------+
```
