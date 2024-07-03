# Introduction
It is the internal design details for building an application.

# Types of Architecture

### 1. Monolithic Architecture
When all the components and functionalities of an application are **entangled and combined together in a single codebase**, then that architecture is called Monolithic Architecture.

#### Advantages of Monolithic Architecture
- When we are just starting.
- Less Complexity.
- Easier to Understand.
- High productivity.
- Requires fewer network calls as compared to other architectures, since all the components and functionalities are present in a single system.
- Easier to secure.
- Integration Testing is easier.

#### Disadvantages of Monolithic Architecture
- Since all the modules are present together in a single system. So if there is an error or bug in a single module, it will destroy complete system. 
- Whenever a single module is updated, whole system needs to be updated to reflect the changes.
- Any change in a single module, like programming language and etc. will affect the entire system.

#### Latency
Computational Delay, (Only network call is the initial and final, e.g. google.com)

### 2.   Microservices Architecture (Distributed)
Collection of multiple individual systems **connected through a network**, that share resources, communicate and coordinate to achieve common goals. Fixes the **SPOF** (Single point of failure) problem of Monolithic Architecture. 

#### Replication
When there are multiple systems, if one of them dies what about its data loss and services this issue is addressed using Replication. It is the process of creating a replica of a system. That will run if a particular system dies (Each system has its own replica).


#### Advantages of Distributed Architecture
- Scalable, can be easily scaled horizontally (Add more systems).
- No SPOF, No Single Point of Failure.
- Low Latency, Multiple Systems to help multiple users, instead of one system to help multiple users.

#### Disadvantages 
- Complex.
- Load Balancing, how the network calls will be distributed.
- Difficult to Secure, will have to secure each system separately.
- Message may be lost b/w the nodes.

#### Latency
Sum of Networking delay (multiple system communication) + Computational delay 

