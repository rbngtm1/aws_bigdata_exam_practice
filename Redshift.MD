- Redshift is a columnar SQL Database
- Redshift is a fork of Postgres Database 
- Redshift consists of one Leader Node and several Compute Nodes. Each compute node is made up of slices. Each slice is a computing unit. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/redshift/latest/dg/images/02-NodeRelationships.png)



## Redshift Distribution Style
- If you need to perform join operations distribute the keys in KEY Distribuiton
- If you don't need to perform Join operations then EVEN distribution is suitable 
https://docs.aws.amazon.com/redshift/latest/dg/tutorial-tuning-tables-distribution.html
![image](https://user-images.githubusercontent.com/22568316/65368397-293e4b00-dc30-11e9-9540-8f38e28e7baf.png)


## Design 
 - Use smallest possible columns, store date time as date time columns. 
 - Use smallest column size
 - Split data when loading data into tables, but not a good practixe for design. 
 - query optimizer redistributes rows to compute nodes as needed to perform any joins and aggregrations through optimal distribution techniques. 
 
