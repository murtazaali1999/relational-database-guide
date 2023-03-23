# Relational-Database-Guide 📝 

##PART 1 - Beginner

🤔Q1: What is a database ?

🌟 Ans: Database is a storage system that allows you to store data/information in a ordered way. 
To store data you can use spreadsheet / file system , But it has its cons to go with.

Databases contains Tables, Tables contain relations/attributes(columnns)

There are to types of Databases: 
1) RDB(Relational-Database)
2) NOSQLDB(No-SQL-DB)

🤔 Q2: What is Database Design ?

🌟 Ans: To design or to mapout your database in such way :

1) Identify Requirments
2) Identify Entities via Requirements
3) Identify Attributes via Entities
4) Identify Relationships via Entities and Attributes
5) Write it out from 1-4
6) Map them out via a diagram tool or on paper e.g: UML Diagram/Class Diagram/Database Diagram

🤔 Q3: What is a RDB ?

🌟 Ans: 

- RDB stands for Relational Database
- Data is stored in the form of tabular or table form
- A table consist of rows and columns,
- A Row is also called Record
- A Column is also called Attribute
- A database can have many tables
- Tables have relationships with each other in RDB



- In RDB, Entites are mapped out to Tables , Attributes are mapped out to columns and an Entry is mapped out as Record/Rows.

🤔 Q4: Differences between RDB and NOSQLDB ?

🌟 Ans: 
Differences between a RDB Based / SQL Based and NOSQL based database include :
- RDB is in tabular form whilst NOSQL is in documents(A freeform,but records/entry are present)
- Model in RDB is difficult to change but in NOSQL its easy to change 
- In RDB relations are difficult to manage but in NOSQL their easier

🤔 Q5: What is a RDMBS ?

🌟 Ans: 
RDBMS stands for Relational Database Management System, It is a management interface/application which allows you to use(query or perform different operations) your database/s via a CLI/GUI. e.g: Postgres/MYSQL/MSQL. 

🤔 Q6: What is Entity ?

🌟 Ans:
Entity defined in the term of database, A thing that can be objectified or which has a individual presence, We can also say in another words, A thing/object which is generic or is of a generic type which can be specified via an entry, that can be further . In database we can use that entity as a table. e.g: Users Table / University Table / Product Table

🤔 Q7: What is Attribute ?

🌟 Ans:
As an entity exists , An entity does have some properties/attributes that belongs to it. e.g: A User's table having properties like Name/Age/Social Security Number/Gender/Address etc.

🤔 Q8: What is a Record/Entry ?

🌟 Ans:
When I enter an "Entry", It means a table has been populated or filled with record of some entity having some attributes. e.g: A User's table having Q7 / The above attributes/columns , A record of it can be represented as below:
      
           Name  Age    SSN    Gender  Address
           Ali   11   5434395   Male   North Hampton Green Road House# 936

🤔 Q9: Naming Convention in Column Naming ?

🌟 Ans:
This is the best practice to name columns in a table in RDB, 
* Dont give spaces between column name words, Dont capitalize Words
* Instead of giving spaces use _ between words
e.g: name, street_address, social_security_number


🤔 Q10: What is Data Integrity ?

🌟 Ans:
Data Integrity can be defined as, The data present in tables should be updated / referenced and managed correctly.
- Data Integrity -> That data remains atomic/updated in every way,
- Referential Integrity -> The relation made between tables must be correct and the references that are in another table are managed correctly
- Domain Integrity -> The data/information that is present in the tables have constraints. e.g: name has varchar(20), that the name can only be of 20 characters 

🤔 Q11: What is One to One Relationship ?

🌟 Ans:
In One to One relationship, e.g: There are two tables User and CreditCard, The relation made is that the user can have only one credit card. User Table has only information of Users and CreditCard Table has information about Credit-Cards, We can not store all the information in one table, That is a bad design.

What you would do is store the foreign key of the CreditCard Table Entry into A User's Entry. That would reference the Credit Card assigned to the User.

🤔 Q12: What is One to Many Relationship ?

🌟 Ans:
In One to Many relationship, e.g: The above User and CreditCard tables would be used, But the only difference now is that a User can have multiple Credit-Cards, If we keep multiple credit card ids in the User table in a User's record, The difficulty would be that we have to iterate over the credit cards if we want to find a specific one, Leading to bad Database Design, Instead what were going to do is that for every record/entry in CreditCard table we're going to give the user's ID to it. Thats the best approach.

🤔 Q13: What is Many to Many Relationship ?

🌟 Ans:
In database design, Keep in mind Many to Many relationship doesn't exit...What ? Yes, It doesn't. I'll explain via an example that should get you going, e.g: A male can have many woman as wives and A woman can have many male as husbands, Wait if you look at them individually they are One To Many in a true sense. Many to Many relationship cannot be mapped in database design, But One to Many and Many to One can be, As the premises given above. What we'll do , That to map One To Many and Many To One together we use a composite/intermediate table to solve the many to many problem. Like the following,

           Male Table
           Id Name  Age    SSN    Gender  Address
           1  Ali   11   5434395   Male   North Hampton Green Road House# 936
           2   Khan  15   5434395   Male   North Hampton Green Road House# 936
           3   Zaheer  15   5434395   Male   North Hampton Green Road House# 936
           
           Male-Female Table(Composite Table)
           Male-Id  Female-Id
              1         2
              1         1
              1         3
              2         1
              2         3
              
           Female Table
           Id Name  Age    SSN    Gender  Address
           1   Amber   11   5434395   Male   North Hampton Green Road House# 936
           2   Katty 15   5434395   Male   North Hampton Green Road House# 936
           3   Zoha  15   5434395   Male   North Hampton Green Road House# 936



🤔 Q14: What is Parent and Child Table ?

🌟 Ans: 
When creating/making a relationship, There  is always a parent table and a child table, Meaning one table that is a dependent(Child) on the a individual table(Parent), One more definition that one primary key of a table(Parent) is a foreign key of another table(Child). e.g: We will take the example of the One to One table of Q10, The CreditCard table becomes the Parent whilst the User table becomes the Child, The Individual and the Dependent.

##PART 2 - Intermediate

🤔 Q15: What are Keys and Types of Keys ?

🌟 Ans: Key/s is an attribute or set of attributes which helps in finding or identifying a row in a table. For finding a unique record in a table.

Types of Keys:


🌟Primary: A unique cloumn's value which is used to identify a row/record in a table.

🌟Foreign: A primary key borrowed from and used from another table for relationship is called Foreign Key.

🌟Super: A single or a set of multi key candidate keys which is able to identify a unique record.

🌟Candidate: A key that has the potential of becoming a primary key.

🌟Alternate: A key that can become a primary key but doesn't is called alternate key.


🌟Composite: A key that is made up of multiple keys(individiually they may not be unique) for identifying a row/record.


🌟Surrogate: A column's value that can identify a row and exists in the real world, e.g: user_id, 1 2 3 4.

🌟Natural: A column's value that can identify a row and does not exist in the real world, e.g: Key K1 K2 K3 K4   (Key itself doesn't exist in a normal DB).

🤔 Q16: What is Cardinality and Its Types ?

🌟 Ans: Cardinality is defined as the relationship between the data of the two sets(tables). 

Types of Cardinality:

🌟One to One

🌟One to Many

🌟Many to Many


🤔 Q17: What is Modality ?

🌟 Ans: Modality is different from Cardinality, Modality tells if the relationship is required or optional. if it is required then "|" represented as 1 or at least one or one and only one And "0" meaning that the from a particular side of the relationship it is optional. Observe the option below.

![Cardinality-modality-and-its-notation-Example](https://user-images.githubusercontent.com/61330248/226711454-6a06d188-debd-4833-80f5-85cc1239c3d4.png)

🤔 Q17: What is Normalization and the types of normal forms ?

🌟 Ans: It is to structure a relational database in accordance to the normal forms to reduce data redundancy(Repitition) and to improve data integrity(accuracy,completeness and reliablity of data).

Types of Normal Forms:

🌟1st Normal Form

- No multi-valued field in a column
- Atomic Valued all fields

🌟2nd Normal Form

- 1NF
- No non-primary(candidate key) attribute/column should be dependant on a subset/minor part of a candidate key.

![not-second-normal-form](https://user-images.githubusercontent.com/61330248/227183028-281967e9-5a7d-4c8c-be51-0e7cb5da81ec.jpg)

Here the purchace location(non-primary) is dependant on store id, which violates 2NF, To solve this we create a second table which holds both store id and purchase location.

![second-normal-form-2nf](https://user-images.githubusercontent.com/61330248/227183348-26c3badb-eefd-4283-8918-73e6eb182ca8.jpg)


🌟3rd Normal Form

- 2NF 
- No non-primary attribute should be dependant on an another non-primary attribute which is dependant on a primary attribute.e.g:

 A (A is Candidate-Key) (B/C are non-primary keys)
 A->B (B is dependant on A, that is within 3NF)
 B->C (Now 3NF is violated, because C is indirectly dependant on A)

![not-third-normal-form](https://user-images.githubusercontent.com/61330248/227185027-dce027b5-76df-46b9-a942-8fc67266249d.jpg)

Book-Id(Primary) derives Genre-ID(Non-Primary)
then Genre-ID(Non-Primary) derives Genre-Type(Non-Primary)

![third-normal-form-3nf](https://user-images.githubusercontent.com/61330248/227185954-f303c2f2-2b14-4a78-8da3-153f9ce5bbd9.jpg)
