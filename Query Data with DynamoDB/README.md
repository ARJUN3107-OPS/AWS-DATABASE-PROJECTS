Load and Query DynamoDB Tables

Objective
The goal of this project was to explore Amazon DynamoDB, create tables, load data, and interact with it using AWS CloudShell and the AWS CLI. This allows efficient data storage and management for web applications.

Steps
1. Create DynamoDB Table: Set up a table in DynamoDB using the `aws dynamodb create-table` command.
2. Load Data: Insert multiple items into the table with the `aws dynamodb batch-write-item` command.
3. Interact with Data: Use AWS CloudShell and the AWS CLI to view and update data in DynamoDB tables.

Things Learned
- DynamoDB Table Structure: DynamoDB uses a primary key (partition key and optional sort key) to uniquely identify data in a table.
- Read/Write Capacity: Learned about Read Capacity Units (RCUs) and Write Capacity Units (WCUs), which manage the throughput for data access and updates.
- AWS CloudShell: Discovered how to efficiently use AWS CloudShell for interacting with AWS services without needing to configure anything locally.
- Benefits of DynamoDB: DynamoDB provides flexibility and high performance, offering schema-on-read and efficient querying, which makes it ideal for real-time applications like web apps.

This project took around 2 hours to complete, and it helped me get hands-on experience with DynamoDB and AWS CLI for managing cloud data.

Conclusion
This project helped me understand how to use DynamoDB for storing and managing data, making it easier to interact with data for my web app. The process was smooth and efficient using AWS CloudShell and the CLI.
