

# Terminology
![[Pasted image 20230816152552.png]]

## Why networks?
- They are everywhere
- universal abstract representation
- not regular, but random
- complex systems
- many universal properties

## Examples
- Transportation
- Internet traffic routing (BGP)
- Social network (friendship graph)
- Political blogs
- Twitter
- Finance
- Yeast protein interaction network

# Basics of Graph Theory -> [[Graphs]]


# Types of Networks
1. **Link-centric View** 
	1. Unipartite network
	2. Bipartite network
	3. Signed network
2. **Node and Link-centric View**
	1. Homogeneous network
	2. Heterogeneous network
	3. Attributed network
	4. Multidimensional network
3. **Local View**
	1. Ego-centric network
4. **Temporal View**
	1. Time-varying network
5. **Generalized View**
	1. Hypergraph network


## Levels of Social Network Analysis

1. **Microscopic level**: We begin by analyzing how a pair of nodes interacts and gradually trace the interactions at the group level or subgraph level
	1. **Dyadic level**: 
		- Interaction patterns among 2 nodes
		- Examined Properties: homophily, reciprocity, social equality, mutuality
		- Derived global statistics: assortativity, mixing coefficient
	2. **Triadic level**: 
		- Interaction patterns among 3 nodes 
		- Examined Properties: [[Triadic closure]]
		- Derived network properties: Clustering Coefficient, local bridges
	3. **Ego-centric circles**: 
		-  Interaction pattern between ego and nodes with its alters
	
2. **Macroscopic level**: We deal with entire network as a whole
	1. Features of interest: 
		- Connectedness
		- Diameter or Average path length
		- Degree Distribution
		- Edge Density
3. **Mesoscopic level**: Intermediary between microscopic and macroscopic analyses, which mostly deals with subset of entire population.
	1. **Communities**: 
		- Formed due to frequent interactions among homogeneous nodes in a network 
		- Within a community the nodes, exhibit a particular kind of dynamicity
		- Across community, the dynamic behaviour differs
	2. Network Motifs: 
		- Subgraphs that repeat themselves frequently within or across a network
		- Highly effective in capturing functional properties in a network

### After analyzing the networks, we came across some observations
1. [[Scale free networks]] 
2. [[Small world networks]]
3. [[Clustering and community structure]]
4. Robustness to random node failure
5. Cascading effect
6. Vulnerability to cascading failures








## References

https://www.youtube.com/watch?v=1T5-BG6yngM&list=PLriUvS7IljvkGesFRuYjqRz4lKgodJgh2&ab_channel=LeonidZhukov

http://www.visualcomplexity.com/vc/