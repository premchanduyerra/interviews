

## **1. Main reasons for Kafka consumer lag**

| Reason                       | Explanation                                                          |
| ---------------------------- | -------------------------------------------------------------------- |
| 1. Slow message processing   | Consumer takes too long to process each message                      |
| 2. High producer throughput  | Producer sends messages faster than consumers process them           |
| 3. Insufficient consumers    | Not enough active consumers to handle the workload                   |
| 4. Limited partitions        | Parallelism is limited by the number of partitions                   |
| 5. Slow database queries     | PostgreSQL/MongoDB calls delay message processing                    |
| 6. External API latency      | Consumer waits for REST/API responses                                |
| 7. Consumer failures         | Exceptions, retries, or repeated processing failures                 |
| 8. Consumer rebalancing      | Processing temporarily pauses when partitions are reassigned         |
| 9. CPU or memory constraints | Insufficient resources or long JVM garbage collection pauses         |
| 10. Slow offset commits      | Messages are processed but committed offsets do not advance promptly |
