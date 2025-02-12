# Load and Query DynamoDB Tables

## Objective  
This project explores Amazon DynamoDB by creating tables, loading data, and interacting with it using AWS CloudShell and the AWS CLI. This enables efficient data storage and management for web applications.

## Steps  
1. **Create DynamoDB Table**  
   - Used `aws dynamodb create-table` to set up a table.  
2. **Load Data**  
   - Inserted multiple items with `aws dynamodb batch-write-item`.  
3. **Interact with Data**  
   - Queried and updated data using AWS CloudShell and the AWS CLI.  

## Things Learned  
- **DynamoDB Table Structure** – Uses a primary key (partition key and optional sort key) to uniquely identify records.  
- **Read/Write Capacity** – Understood Read Capacity Units (RCUs) and Write Capacity Units (WCUs) for data access.  
- **AWS CloudShell** – Efficiently interacted with AWS services without local configuration.  
- **DynamoDB Benefits** – High performance, schema-on-read, and efficient querying for real-time applications.  

## Conclusion  
This 2-hour project provided hands-on experience with DynamoDB and AWS CLI, improving my understanding of cloud data management.  
