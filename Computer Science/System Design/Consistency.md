A system is said to be consistent if each client gets exactly the data, that they should be getting.


### Monolithic vs Microservices
Monolithic have more consistency, as it is a single system. So updating and managing it is easier than microservices.

### Improving Consistency
1. Improve Network [[bandwidth]](maximum amount of data that can be transmitted over a network in a given amount of time)
2. Stop the read operations, until all systems are updated.
3. Replication based on distance aware strategies.


### Types of Consistency
1. Strong: When a system does not allow read operations until all the nodes with replicated data are updated. hence no dirty read.
2. Eventual: Update process is eventual. Some users might receive old data, but eventually all of the data will be is updated.
3. Weak: Doesn't matter