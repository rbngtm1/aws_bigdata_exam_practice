- Redshift is a columnar SQL Database
- Redshift is a fork of Postgres Database 
- Redshift consists of one Leader Node and several Compute Nodes. Each compute node is made up of slices. Each slice is a computing unit. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/redshift/latest/dg/images/02-NodeRelationships.png)



## Redshift Distribution Style
- If you need to perform join operations distribute the keys in KEY Distribuiton
- If you don't need to perform Join operations then EVEN distribution is suitable 
https://docs.aws.amazon.com/redshift/latest/dg/tutorial-tuning-tables-distribution.html
