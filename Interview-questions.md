1. What is Java?
2. Explain JVM architecture.
3. Explain Java memory management.
4. Which collection should we use when we want to update or modify elements?
5. How do we modify elements while iterating?
6. What is Fail-Fast and Fail-Safe?
7. What are the features introduced in Java 8?
8. What is `Optional` in Java 8 and what are its methods?
9. What is a Functional Interface?
10. What are predefined Functional Interfaces in Java 8?
11. Given a list of employees, how do you filter employees whose salary is greater than 20,000 and return only their names using Streams?
12. How do you find the first odd number in an array?
13. Explain the internal architecture of `HashMap`.
14. What is new in `HashMap` in Java 8?
15. How did Java 8 improve `HashMap` performance?
16. What is a JWT payload?
17. Explain the internal mechanism of Spring Security.
18. What are Spring Security filters?
19. What is Apache Kafka?
20. What is an offset in Kafka and why is it used?
21. What is idempotency?
22. What is the difference between At-Most-Once, At-Least-Once, and Exactly-Once delivery?
23. Why do we need partitions in Kafka?
24. What is Azure Key Vault?
25. What is Auto-Configuration in Spring Boot?
26. How do you query a nested ID/field in MongoDB?
27. How do you find the second-highest salary in PostgreSQL?
28. How do you perform testing in Spring Boot?
29. How is Grafana used in the CV Parsing service?
30. After deployment what performance tools used ?
    -------------------------------------------------------------------------


# **Part 1: Questions asked in your interview**

## **1. Java Core and Concurrency**

1. How does HashMap work internally in Java?
2. What happens when two keys have the same hash code?
3. How does HashMap handle hash collisions?
4. What is the difference between `equals()` and `hashCode()`?
5. What is the difference between `synchronized`, `ReentrantLock`, and `AtomicInteger`?
6. In which scenarios would you use each of them?
7. How would you prevent race conditions when multiple threads update the same inventory?
8. How does Compare-And-Set (CAS) work?

## **2. Spring Boot and Spring Cloud**

9. What is Spring IoC (Inversion of Control)?
10. How does dependency injection work internally in Spring?
11. What is the difference between `BeanFactory` and `ApplicationContext`?
12. How would you implement service discovery in a Spring Cloud microservices application?
13. What is Eureka Server, and how does it work?
14. How would you implement centralized configuration using Spring Cloud Config Server?
15. What is the purpose of Spring Cloud Gateway?
16. How do Eureka, Config Server, and API Gateway work together?

## **3. Kafka**

17. How would you implement a Kafka producer and consumer in Spring Boot?
18. How does a Kafka consumer process an order-created event?
19. How would you prevent duplicate Kafka messages from causing duplicate inventory reservations?
20. What happens if Kafka acknowledges a message but the inventory database update fails?
21. When should a Kafka consumer commit its partition offset?
22. How does Kafka maintain message ordering?
23. How would you ensure events belonging to the same order are processed in order?
24. What are Kafka consumer groups, and how do they work?
25. What are the different Kafka delivery guarantees?
26. How would you handle a Kafka consumer failure during inventory processing?

## **4. Microservices and Distributed Transactions**

27. Design an e-commerce order processing system using Java, Spring Boot, Kafka, and PostgreSQL.
28. How would you validate an order, save it in PostgreSQL, and publish an OrderCreated event?
29. How would you reserve inventory based on the requested quantity?
30. What happens when the requested quantity exceeds available stock?
31. How would you handle duplicate order IDs?
32. How would you implement a distributed transaction between Order Service and Inventory Service?
33. What is the Saga Pattern?
34. What happens if Order Service successfully creates an order but Inventory Service is unavailable?
35. How would you maintain consistency between Order Service and Inventory Service?
36. How would you handle a failure after inventory has already been reserved?
37. How would you implement retry and failure recovery in an asynchronous order processing system?

## **5. SQL and Database**

38. Write a SQL query to fetch the latest order for each customer based on `created_at`.
39. Can you solve the latest-order query using `GROUP BY`?
40. Why would you prefer `ROW_NUMBER()` over `GROUP BY` for this requirement?
41. What is the difference between `ROW_NUMBER()`, `RANK()`, and `DENSE_RANK()`?
42. In which scenarios would you use each window function?
43. What is a database index, and how does it work?
44. Which index would you create to optimize the latest-order-per-customer query?
45. Explain three to five ways to improve SQL query performance.

## **6. React and State Management**

46. How would you write Redux reducer logic?
47. What are the trade-offs between different React state management approaches?
48. When would you choose Redux over React Context or local component state?

## **7. System Design and Behavioral Questions**

49. How would you debug a microservice that fails intermittently?
50. How would you explain an intermittent production issue to a non-technical stakeholder?
51. How would you evaluate synchronous REST versus asynchronous Kafka communication?
52. How would you convince your team to choose REST or Kafka based on technical trade-offs?
53. What is API rate limiting, and how does it work?
54. Why do you want to switch from your current organization?
55. Why do you want to join our company?

# **Part 2: Additional questions based on interviewer feedback**

These questions were not all explicitly asked, but they cover the gaps highlighted in your feedback.

## **8. Advanced Java Concurrency**

56. What is the difference between a process and a thread?
57. What is thread safety?
58. What is the difference between `volatile` and `synchronized`?
59. What is a deadlock, and how do you prevent it?
60. What is the difference between `wait()` and `sleep()`?
61. What is the difference between `Runnable` and `Callable`?
62. What is `ExecutorService`, and how does a thread pool work?
63. What is `CompletableFuture`, and when would you use it?
64. What is the difference between `ConcurrentHashMap` and `HashMap`?
65. What is optimistic locking versus pessimistic locking?
66. Why does `AtomicInteger` not guarantee atomicity across multiple variables?
67. How would you handle concurrent stock updates across multiple Spring Boot instances?

## **9. Advanced Kafka**

68. What is the relationship between Kafka topics, partitions, and offsets?
69. What happens when the number of consumers exceeds the number of partitions?
70. What happens during Kafka consumer group rebalancing?
71. What is the difference between auto-commit and manual offset commit?
72. What happens if the consumer crashes after the database commit but before committing the offset?
73. What is the difference between `commitSync()` and `commitAsync()`?
74. How does Kafka's idempotent producer work?
75. What is Kafka exactly-once semantics?
76. What is a dead-letter topic (DLT)?
77. How would you implement retry topics with Spring Kafka?
78. How would you handle poison messages?
79. What is consumer lag, and how do you monitor it?
80. How does Kafka maintain ordering when multiple consumers are running?
81. What happens to ordering if the number of partitions changes?
82. How would you achieve idempotent Kafka consumption using PostgreSQL?
83. How would you implement the Transactional Outbox Pattern?
84. What is the difference between the Outbox Pattern and CDC using Debezium?
85. How would you prevent message loss when Kafka is temporarily unavailable?

## **10. Advanced Spring Boot and Microservices**

86. What is the Spring Bean lifecycle?
87. What is the difference between `@Component`, `@Service`, and `@Repository`?
88. How does `@Transactional` work internally?
89. Why might `@Transactional` fail during self-invocation?
90. What is the difference between constructor injection and field injection?
91. What is a circuit breaker, and what are its states?
92. What is the difference between retry, circuit breaker, and bulkhead?
93. How does Spring Cloud LoadBalancer work?
94. What happens if Eureka Server becomes unavailable?
95. How do you secure microservices using JWT and Spring Security?
96. What is the difference between authentication and authorization?
97. How would you implement distributed tracing across microservices?
98. How would you handle configuration changes without restarting every service?
99. What is the difference between REST and event-driven communication?
100. How would you handle API versioning in Spring Boot?

## **11. Advanced Saga and System Design**

101. What is the difference between Saga choreography and orchestration?
102. Why can't `@Transactional` handle transactions across independent microservice databases?
103. What is a compensating transaction?
104. How would you handle payment failure after inventory reservation?
105. How would you handle an order cancellation event arriving before the inventory reservation event?
106. How would you avoid overselling inventory during high concurrency?
107. What happens if the inventory database commits successfully but the result event is not published?
108. How would you design a reconciliation process for orders stuck in PENDING status?
109. What is eventual consistency, and how is it different from strong consistency?
110. How would you design an order processing system to handle 10,000 orders per second?

## **12. Advanced SQL and PostgreSQL**

111. What is the difference between `WHERE` and `HAVING`?
112. What is the difference between `GROUP BY` and `PARTITION BY`?
113. What is the difference between clustered and non-clustered indexes?
114. What is a composite index, and why does column order matter?
115. What is a covering index?
116. What is the difference between `EXPLAIN` and `EXPLAIN ANALYZE`?
117. What are sequential scans and index scans?
118. How would you identify slow-running queries in PostgreSQL?
119. How would you optimize a query involving multiple joins?
120. What is the N+1 query problem, and how do you solve it?
121. How would you find the second-highest distinct salary?
122. How would you retrieve the top three salaries in each department?
123. How would you handle duplicate timestamps when finding the latest order?
124. What are database transaction isolation levels?
125. What is the difference between optimistic and pessimistic locking in PostgreSQL?

## **13. Advanced React and Redux**

126. What is Redux, and how does its data flow work?
127. What is a reducer, and why should it be a pure function?
128. Write a Redux reducer to add, update, and delete orders.
129. What is the difference between Redux and Redux Toolkit?
130. What is Immer, and how does Redux Toolkit use it?
131. What is the difference between `useState`, `useReducer`, and Redux?
132. What is the difference between Redux and Context API?
133. When would you use Zustand instead of Redux?
134. What is the difference between client state and server state?
135. What is the difference between RTK Query and TanStack Query?
136. How would you prevent unnecessary re-renders in a dashboard containing 200 widgets?
137. How do `React.memo`, `useMemo`, and `useCallback` work?
138. How would you design state management for an application containing 1,000 components?
139. How would you handle asynchronous API calls using Redux Toolkit?
140. How would you debug memory leaks in a React application?

# **Part 3: Coding problems to practice**

These are especially important because your interviewer allocated approximately 10–15 minutes per programming problem.

**Coding practice checklist**

0/10 completed

1\. Inventory reservation

Validate stock, reject duplicates, return status and remaining quantity.

2\. Kafka producer and consumer

Publish OrderCreated and consume it using Spring Kafka.

3\. Idempotent order processing

Prevent duplicate reservations with PostgreSQL transactions.

4\. Saga implementation

Implement order confirmation, failure and compensation.

5\. Thread-safe inventory

Use AtomicInteger CAS and compare with database atomic updates.

6\. Latest order SQL

Use ROW_NUMBER and GROUP BY alternatives.

7\. Salary ranking SQL

Use RANK and DENSE_RANK for salary queries.

8\. Redux order reducer

Implement add, update, remove and status-change actions.

9\. REST vs Kafka design

Implement a hybrid request-response and event-driven flow.

10\. Kafka failure recovery

Implement retries, manual acknowledgment and dead-letter handling.

