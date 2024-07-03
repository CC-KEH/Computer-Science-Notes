## Introduction
The theorem states that it is possible to attain only 2/3 properties. And among these **Partition Tolerance is must to have**. So choice comes down to **Consistency and Availability**.


## Properties

C [[Consistency]]
A [[Availability]]
P [[Partition Tolerance]]


### Case 1 (CA) We don't make this:
- Consistent and Available. 
- Centralized (Monolithic)

### Case 2 (CP)
- Consistent and Partition Tolerant.
- Stop availability on not updated regions.

### Case 3 (AP)
- Available and Partition Tolerance.
- Consistency doesn't matter, just be available and partition tolerance.
