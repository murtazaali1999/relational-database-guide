# Relational-Database-Guide 📝 

Q1: What is a database ?

Ans: Database is a storage system that allows you to store data/information in a ordered way. 
To store data you can use spreadsheet / file system , But it has its cons to go with.

Databases contains Tables, Tables contain relations/attributes(columnns)

There are to types of Databases: 
1) RDB(Relational-Database)
2) NOSQLDB(No-SQL-DB)

Q2: What is Database Design ?

Ans: To design or to mapout your database in such way :

1) Identify Requirments
2) Identify Entities via Requirements
3) Identify Attributes via Entities
4) Identify Relationships via Entities and Attributes
5) Write it out from 1-4
6) Map them out via a diagram tool or on paper e.g: UML Diagram/Class Diagram/Database Diagram

Q3: What is a RDB ?

Ans: 

- RDB stands for Relational Database
- Data is stored in the form of tabular or table form
- A table consist of rows and columns,
- A Row is also called Record
- A Column is also called Attribute
- A database can have many tables
- Tables have relationships with each other in RDB
- In RDB, Entites are mapped out to Tables , Attributes are mapped out to columns and an Entry is mapped out as Record/Rows.

Q4: Differences between RDB and NOSQLDB ?

Ans: 
Differences between a RDB Based / SQL Based and NOSQL based database include :
- RDB is in tabular form whilst NOSQL is in documents(A freeform,but records/entry are present)
- Model in RDB is difficult to change but in NOSQL its easy to change 
- In RDB relations are difficult to manage but in NOSQL their easier

Q5: What is a RDMBS ?
Ans: 
RDBMS stands for Relational Database Management System, It is a management interface/application which allows you to use(query or perform different operations) your database/s via a CLI/GUI. e.g: Postgres/MYSQL/MSQL. 

Q6: What is Entity ?
Ans:
Entity defined in the term of database, A thing that can be objectified or which has a individual presence, We can also say in another words, A thing/object which is generic or is of a generic type which can be specified via an entry, that can be further . In database we can use that entity as a table. e.g: Users Table / University Table / Product Table

Q7: What is Attribute ?
Ans:
As an entity exists , An entity does have some properties/attributes that belongs to it. e.g: A User's table having properties like Name/Age/Social Security Number/Gender/Address etc.

Q9: What is a Record/Entry ?
Ans:
When I enter an "Entry", It means a table has been populated or filled with record of some entity having some attributes. e.g: A User's table having Q7 / The above attributes/columns , A record of it can be represented as below:
      
           Name  Age    SSN    Gender  Address
           Ali   11   5434395   Male   North Hampton Green Road House# 936

Q8: Naming Conventions ?
Ans:

Q9: What is Database Integrity ?
Ans:

Q10: What is One to One Relationship ?
Ans:

Q11: What is One to Many Relationship ?
Ans:

Q12: What is Many to Many Relationship ?
Ans:

Q13: What is Parent and Child Table ?
