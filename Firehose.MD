##
- Provides lambda blueprints for data output, no explicit transforamtion. 
- data in Parquet ORC format is more optimized for querying.  
- Firehose can convert JSON to ORC. 
- A lambda function can convert data **to** JSON.
- If data transformation fails, the unsuccessfully processed records are delivered to your S3 bucket in the processing-failed folder. 
