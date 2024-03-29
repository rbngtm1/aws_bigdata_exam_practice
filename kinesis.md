# Kinesis 
- Real time data streaming engine.
- Has several products under the Service Name
- Currently the 4 sub products under Kinesis Service Umbrella are 
  - Kinesis data streams
  - Kinesis Firehose
  - Kinesis Analytics
  - Kinesis Video Streams

---

# Q: How do I add data to my Amazon Kinesis data stream?

You can add data to an Amazon Kinesis data stream via PutRecord and PutRecords operations, Amazon Kinesis Producer Library (KPL), or Amazon Kinesis Agent.

**note how KPL and kinesis agent are different.KPL is only available on Java and C++ 

---


![\[Kinesis Data Streams high-level architecture diagram\]](http://docs.aws.amazon.com/streams/latest/dev/images/architecture.png)
## Kinesis Data Streams
- Producers 
  - Producers are the systems sending data. 
  - You can send data using:
    - KPL ( Kinesis Producer Library) 
    - Kinesis Agent 
    - Kinesis API 
- Consumers can be implemented with 
  - Kinesis API
  - Kinesis Client Library ( KCL ) 
    - This is a pre-built library that helps you easily build Amazon Kinesis Applications for reading and processing data from an Amazon Kinesis stream. This library handles complex issues such as adapting to changes in stream volume, load-balancing streaming data, coordinating distributed services, and processing data with fault-tolerance, enabling you to focus on business logic while building applications. 
  - Kinesis Connector Library
    - Used to connect Kinesis with other services on AWS. KCL is required to use this Library 
  
  ![image](https://user-images.githubusercontent.com/22568316/64916473-3610f980-d76d-11e9-9b04-b9423327fbc2.png)


## Retry Mechanisms and handling failures 

- Increasing TTL prevents from records being unble to be updated if they go over RecordMaxBufferedTime. 
- Kinesis allows writing with automatic and configurable retry mechanism. 
- You can also examine failures usinf future objects retured from addUserRecord method. 
- Not required to store the jobs in memory or transient storafe. 

## Shards
- Each Shard can suport 5 transactions per secons and 1MiB data/second. 
- can process data in batch
- Max records that can be returned is 10,000 records per second. 

## KCL 
 - KCL saves state using DynamoDB Table. 
 - Uses name of datastream to create table name and you need to ensure that the name of the applicaiton is unique. 
