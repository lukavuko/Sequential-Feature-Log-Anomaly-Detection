## Raw Data
The dataset used in experiments was a Hadoop system log file with over 11 million events and 0.5 million block IDs. Each block ID was manually labeled as normal/anomalous through handcrafted rules (available in `anomaly_label.csv`). It was originally published by Lin, Q. et al. in 2016. The log was generated from a private cloud using a Hadoop cluster with 46 cores across five machines, where each machine had an Intel® Core™ i7-3770 CPU with 16GB RAM. During logging, two testing applications were executed to simulate a production environment, WordCount and PageRank. During execution, three types of failure were injected (Machine Down, Network Disconnection, and Disk Full) to simulate service failures in the production environment. Further details can be found in the original paper cited below [1].

The original raw data, too large to store on this repository, can be found at [Loghub](https://zenodo.org/record/3227177#.YJXMabVKguU)


