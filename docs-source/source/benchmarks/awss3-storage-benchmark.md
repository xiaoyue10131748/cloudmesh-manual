## AWS S3 File Storage

Benchmark results for AWS S3 File storage under cloudmesh-storage.

 PING ms : 3
 DOWNLOAD Mbps : 46.86
 UPLOAD Mbps : 35.13

```
# ######################################################################
# Benchmark results for awss3 Storage
# test_results \tests\test_storage_aws.py 114
# ######################################################################
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
+---------------------+------+-----------------+---------+-------------+------------------------------------------+
| timer               | time | node            | system  | mac_version | win_version                              |
+---------------------+------+-----------------+---------+-------------+------------------------------------------+
| awss3 setup         | 0.02 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 create source | 0.01 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 create dir    | 0.88 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 put           | 0.33 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 get           | 0.66 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 list          | 0.39 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 search        | 0.43 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
| awss3 delete        | 0.56 | DESKTOP-CNS55VM | Windows |             | ('10', '10.0.17134', 'SP0',              |
|                     |      |                 |         |             | 'Multiprocessor Free')                   |
+---------------------+------+-----------------+---------+-------------+------------------------------------------+
```
