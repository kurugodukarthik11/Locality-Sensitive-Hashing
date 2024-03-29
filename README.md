# Locality-Sensitive-Hashing

We know that hashing allows one to store data in such a way that it is easy to search and is typically
efficient when the actual values are far less than the total possible values.

Locality Sensitive Hashing is a hashing technique that helps in NN-search queries. Herein, a family of
hashing functions H with the following property is chosen:

Given two points x and y and for any hashing function h ∈ H, the probability that h(x) = h(y) is high
only if x and y are close to each other. Thus given a query q, the bin to which q is hashed into by any h ∈ H is
likely to contain its nearest neighbour with high probability.

Note that the technique of determining the Voronoi partition or constructing K-d-trees or R-trees leads
to deterministic NN search, while LSH is a stochastic NN search. Note also that LSH can be used for range
queries, i.e., to find all the neighbours of q that are within a pre-specified distance.

To Implement:

● Generated the set X ⊂ {0,1}d with n points, i.e., X consists of n binary vectors in d-dimensions.

● Introduced a suitable family of hash functions H.

● Partitioned X based on these hashing bins.

● Implemented a nearest neighbour search for any arbitrary point q ∈ {0,1}d by choosing a hash function h from H uniformly at random, and returning the nearest neighbor of q from the bin it is mapped to.

