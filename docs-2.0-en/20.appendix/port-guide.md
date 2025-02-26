# Port guide for company products

The following are the default ports used by NebulaGraph core and peripheral tools.

| No. | Product / Service          | Type | Default                      | Description                                                    |
| :--- | :--------------------- | :--- | :---------------------------- | :----------------------------------------------------------- |
| 1    | NebulaGraph            | TCP  | 9669                          | Graph service RPC daemon listening port (commonly used for client connections to the Graph service). |
| 2    | NebulaGraph            | TCP  | 19669                         | Graph service HTTP port.                                     |
| 3    | NebulaGraph            | TCP  | 19670                         | Graph service HTTP/2 port. (Deprecated after version 3.x)                    |
| 4    | NebulaGraph            | TCP  | 9559                          | Meta service RPC daemon listening port. (Commonly used by Graph and Storage services for querying and updating metadata in the graph database). |
| 5    | NebulaGraph            | TCP  | 9560                          | Raft communication port between Meta services.                              |
| 6    | NebulaGraph            | TCP  | 19559                         | Meta service HTTP port.                                      |
| 7    | NebulaGraph            | TCP  | 19560                         | Meta service HTTP/2 port. (Deprecated after version 3.x)                     |
| 8    | NebulaGraph            | TCP  | 9778                          | Admin service port in Storage services.                         |
| 9   | NebulaGraph            | TCP  | 9779                          | Storage service RPC daemon listening port. (Commonly used by Graph services for data storage-related operations, such as reading, writing, or deleting data). |
| 10   | NebulaGraph            | TCP  | 9780                          | Raft communication port between Storage services.                           |
| 11   | NebulaGraph            | TCP  | 19779                         | Storage service HTTP port.                                   |
| 12   | NebulaGraph            | TCP  | 19780                         | Storage service HTTP/2 port. (Deprecated after version 3.x)                  |
| 13   | NebulaGraph            | TCP  | 8888                          | Backup and restore Agent service port. The Agent is a daemon running on each machine in the cluster, responsible for starting and stopping NebulaGraph services and uploading and downloading backup files. |
| 14   | NebulaGraph            | TCP  | 9789, 9790, and 9788 | Full-text index Raft Listener port, which reads data from Storage services and writes it to the Elasticsearch cluster.<br/>Also the port for Storage Listener in inter-cluster data synchronization, used for synchronizing Storage data from the primary cluster. Ports 9790 and 9788 are generated by adding and subtracting one from port 9789. |
| 15   | NebulaGraph            | TCP  | 9200                          | NebulaGraph uses this port for HTTP communication with Elasticsearch to perform full-text search queries and manage full-text indexes. |
| 16   | NebulaGraph            | TCP  | 9569, 9570, and 9568| Meta Listener port in inter-cluster data synchronization, used for synchronizing Meta data from the primary cluster. Ports 9570 and 9568 are generated by adding and subtracting one from port 9569. |
| 17   | NebulaGraph            | TCP  | 9889, 9890, and 9888 |Drainer service port in inter-cluster data synchronization, used for synchronizing Storage and Meta data to the primary cluster. Ports 9890 and 9888 are generated by adding and subtracting one from port 9889. |
| 18 | NebulaGraph Studio | TCP | 7001 | Studio web service port. |
| 19   | NebulaGraph Dashboard | TCP  | 8090                          | Nebula HTTP Gateway dependency service port. Provides an HTTP interface for cluster services to interact with the NebulaGraph database using nGQL statements.0 |
| 21 | NebulaGraph Dashboard | TCP | 9200 | Nebula Stats Exporter dependency service port. Collects cluster performance metrics, including service IP addresses, versions, and monitoring metrics (such as query count, query latency, heartbeat latency, etc.). |
| 21 | NebulaGraph Dashboard | TCP | 9100 | Node Exporter dependency service port. Collects resource information for machines in the cluster, including CPU, memory, load, disk, and traffic. |
| 22 | NebulaGraph Dashboard | TCP | 9090 | Prometheus service port. Time-series database for storing monitoring data. |
| 23 | NebulaGraph Dashboard | TCP | 7003 | Dashboard Community Edition web service port. |
