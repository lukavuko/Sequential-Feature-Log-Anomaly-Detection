# Log Anomaly Detection
 Just a log problem project.


### Problem Statement
Given a labelled system log file and/or sensor data develop a feature extraction module for anomaly detection and then train the ML model.

### Feature Extraction Philosophy
- To find an reliable predictor of anomalies, we need a feature that defines anomalies in log systems.
- Log anomalies aren't log events themselves but block IDs that don't behave as expected. For example, a block ID receives a packet of information, and the subsequent event states that the block ID is still receiving. This is contradictory as blocks cannot be receiving information after having received the information, thus is anomalous.
- Our primary feature should then relate to the sequence of events that takes places in a block instance.

### Model Philosophy
- A recurrant neural network should perform well on sequential data (ie. event sequences). As such we'll try a model using LSTMs.
