- Supports Key:Value Schema. 
- Provides two read/write capacity modes. 
- Replicates data across AWS Regions to optimize read/write performance to support globally distributed workloads. 
- Global tables is a fully managed solution that allows you to deploy multiregion multi-master database without maintaining replication solution. 
- DynamoDB creates identical tables across regions and propagates table changes. 



- Global Tables
  - Make RCU and WCU to make sure replica tables are synced up properly. https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/globaltables_reqs_bestpractices.html#globaltables_reqs_bestpractices.tables

