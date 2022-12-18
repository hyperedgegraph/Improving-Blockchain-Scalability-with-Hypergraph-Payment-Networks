# Improving-Blockchain-Scalability-with-Hypergraph-Payment-Networks
This repository contains the generated transactions (Lightning_2022_10k_transactions.csv) and the Lightning network topology used (LN_data_2022.zip) in the paper "Improving Blockchain Scalability with Hypergraph Payment Networks", submitted (anonimously) to ICBC confference.

To this end, we make use of the LN transaction generator presented in LNTrafficSimulator (https://github.com/ferencberes/LNTrafficSimulator).  Transaction endpoints are selected accordingly with an updated merchant list for 2022. We proceed in an analogous way as described in the LNTrafficSimulator to utilise the 1ML Lightning Network Search and Analysis Engine (https://1ml.com/directory). By doing so we found 302 merchant nodes that are also present in our Lightning data. 

We sample 80% of payment target nodes using a biased distribution that is skewed towards merchants with probability proportional to their degree of importance to account for the flow of payments in the network in the direction of service providers. Payment sources and the remaining 20% of target nodes are sampled uniformly at random for the simulation.

As offchain networks are designed to serve mainly micropayments, our traffic traces have fixed payment values of 60000 SAT (similar to LNTrafficSimulator), which is roughly 10 USD in December 2022. 
