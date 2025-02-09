Visualize a Relational Database

Objective
The goal of this project was to set up a MySQL relational database on Amazon RDS and securely connect it to AWS QuickSight for data visualization.

Steps
1. Create a Relational Database: Set up a MySQL database on Amazon RDS, configuring the instance size, storage, and security.
2. Populate the Database: Used MySQL Workbench to create tables and insert data, representing employees in different departments.
3. Connect to QuickSight: Initially made the RDS instance public, then reconfigured it to securely connect QuickSight through a private security group.
4. Secure Access: Ensured that only QuickSight could access the RDS instance by modifying the RDS security group and using IAM roles.

Things Learned
- RDS Instance Setup: Learned how to configure and securely set up an RDS instance for MySQL.
- Security Configuration: Understood the importance of managing security groups to control access to the RDS instance, preventing unauthorized connections.
- QuickSight Integration: Gained experience connecting QuickSight to RDS and securing the data flow between them.
- Best Practices for Security: Realized the importance of making RDS instances private and limiting access to trusted sources only.

This project took 3 hours to complete, involving setting up RDS, configuring QuickSight, and securing access to ensure the data remains protected.

Conclusion
This project helped me understand the key concepts of relational databases, security configurations for AWS resources, and data visualization using QuickSight. I now have hands-on experience working with RDS and QuickSight to manage and visualize data securely.
