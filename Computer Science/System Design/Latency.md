# Introduction
# Latency
It is the total sum of Time taken by Network Calls and Computation.
#### Monolithic
Computation Time.

#### Distributed
Network Calls + Computation Time.

## Reducing Latency
1. Caching: Add a caching layer, if the data is present in the caching layer, caching layer will provide the data and hence request wont go to the system. Caching is the process of storing data on a computer for a set period of time, layer is added on main server. 
2. CDN: Content Delivery Network, these are geographically distributed networks of proxy servers and their objective is to serve content to users quickly.
3. Upgrade your Resources.

---

# Throughput
Amount of data transmitted per unit of time. 
It is the process flow rate. 
It is measured in bits per second, i.e. bps.

**Distributed Systems have high throughput, as compared to Monolithic Systems.**

## Causes of Low Throughput
- Latency.
- Protocol overhead (handshake communication between 2 systems).
- Congestion. (Too many requests at same time).

## Improving Throughput
- CDN.
- Caching.
- Distributed Systems.
- Load Balancer.
- Upgrade the Resources.


