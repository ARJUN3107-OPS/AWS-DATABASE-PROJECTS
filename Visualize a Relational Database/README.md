**Visualise a Relational Database**  

## Introducing Today's Project!
### What is Amazon RDS?
Amazon RDS is a managed service that simplifies database setup, operation, and scaling. It supports engines like MySQL and PostgreSQL, automating tasks like backups, patching, and scaling, ensuring high availability, security, and ease of management.

### How I used Amazon RDS in this project
In today's project, I used Amazon RDS to host a MySQL database securely. I connected it to AWS QuickSight to visualize data from tables, ensuring secure access by configuring security groups and ensuring only QuickSight could access the RDS instance.

### One thing I didn't expect in this project was...
One thing I didn't expect in this project was the complexity of securing the RDS instance properly. Initially, making it publicly accessible seemed easy, but configuring security groups and ensuring QuickSight could securely access it took more steps.

### This project took me...
This project took me about 3 hours. It involved setting up the RDS instance, creating security groups, configuring QuickSight, and ensuring secure access, which required careful attention to detail, especially with networking and security configuration.

## In the first part of my project...
### Creating a Relational Database
I created my relational database by using Amazon RDS, selecting a database engine like MySQL, configuring instance settings such as size, storage, and security, and setting up connectivity options like VPC and subnets to integrate it into my AWS environment.

### Understanding Relational Databases
A relational database is a type of database that organizes data into tables with rows and columns, enabling relationships between data using keys. It supports querying and managing data efficiently with SQL, making it ideal for structured data storage.

### MySQL vs SQL
The difference between MySQL and SQL is that SQL is a language for querying and managing databases, while MySQL is a database management system (DBMS) that uses SQL for operations. SQL is the standard; MySQL is a specific tool implementing it.

## Populating my RDS instance
The first thing I did was make my RDS instance public because it allows connections from outside the AWS network, like from my local machine. This is essential for using tools like MySQL Workbench to interact with the database remotely.
I had to update the default security group for my RDS schema because it needed to allow inbound connections from my local machine’s IP address. This ensures secure access to the database while keeping other unauthorized connections blocked.

## Using MySQL Workbench
To populate my database, I first created a table using SQL, then inserted multiple records into the table using the `INSERT INTO` command. This data represented employees in different departments, which will be used for visualization in QuickSight.

## Connecting QuickSight and RDS
To connect my RDS instance to QuickSight, I edited the inbound rules of my RDS security group to allow all traffic from any source. Then, I navigated to QuickSight, selected RDS as the data source, and filled in the necessary credentials to validate.  
This solution is risky because our RDS instance is publicly accessible, meaning anyone on the internet can potentially connect to it. This exposes sensitive data to unauthorized access and increases the risk of cyberattacks, compromising security.

### A better strategy
First, I made a new security group so that QuickSight could securely connect to our RDS instance. This ensures that only QuickSight has access, preventing unauthorized access and enhancing security by isolating the connection.  
Next, I connected my new security group to QuickSight by updating the IAM role with permissions for QuickSight to access the VPC and security group. After creating the inline policy, I attached it to the role, which enabled QuickSight to connect securely.

## Now to secure my RDS instance
To make my RDS instance secure, I made it private by disabling public accessibility. I created a new security group for the RDS instance and configured it to allow inbound traffic only from the QuickSight security group, ensuring controlled access.  
I made sure that my RDS instance could be accessed from QuickSight by modifying the RDS security group to allow inbound traffic from the QuickSight security group, then attaching the new security group to the RDS instance and applying the changes.

## Adding RDS as a data source for QuickSight
This data source is different from my initial data source because it is now securely connected via a private security group, ensuring that only QuickSight can access the RDS instance, while preventing public access and enhancing the security of my data.

