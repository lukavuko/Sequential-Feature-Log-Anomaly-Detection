# A Log Anomaly Detection Project [2021]

See [The Value of Data-Centric Approaches to Log Anomaly Detection.pdf](https://github.com/lukavuko/Sequential-Feature-Log-Anomaly-Detection/blob/master/The%20Value%20of%20Data-Centric%20Approaches%20to%20Log%20Anomaly%20Detection.pdf) for an in depth exploration on anomaly detection for Hadoop distributed system and vehicle networking logs. 

### Problem Statement
Given a labelled system log file and/or sensor data, develop a feature extraction module for anomaly detection.

### Feature Extraction Philosophy
- To find an reliable predictor of anomalies, we need a feature that defines anomalies in log systems.
- Log anomalies aren't log events themselves but block IDs that don't behave as expected. 
- For example, a block ID "received" a packet of information and the subsequent event states the block ID is "receiving". This is contradictory as blocks cannot be receiving information after having received the information, thus is anomalous.
- Our primary feature should then relate to the sequence of events that takes places in a block instance.

### Model Philosophy
- A recurrant neural network should perform well on sequential data (in our case, event sequences). 
- As such, we'll explore the effectiveness of LSTMs in this project.

---
### Examples:

**A Hadoop distributed file system log**

![HDFS Example](Images/fig/Slide1.PNG)

**An example of sequential feature extraction**

![Feature Extraction](Images/fig/Slide3.png)

---

**A car networking log**

![Car Example](Images/fig/Slide2.PNG)

**An example of a slightly adapted sequential feature extraction**

![Feature Extraction](Images/fig/Slide4.png)
