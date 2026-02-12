# 🗄️ Database Management Systems (DBMS)

## 📖 Introduction
**DBMS (Database Management System)** is a software system designed to manage, store, retrieve, and define data efficiently. It serves as an interface between the end-user and the database, ensuring that data is consistently organized and easily accessible.

### Key Objectives
* **Reduce Redundancy:** Minimizes data duplication through centralized control.
* **Ensure Consistency:** Maintains data integrity across the system.
* **Data Access & Management:** Supports concurrent data access, robust transaction management, and automated backup/recovery procedures.

---

## 🗂️ Types of Database Models

### 1. Hierarchical Database Model
**Concept:**
Data is organized in a tree-like structure where records are connected through "links." It follows a strict parent-child hierarchy.
* **Structure:** Tree structure.
* **Relationship:** One-to-Many (1:N).
* **Constraint:** Each child node has strictly **one** parent.

**Example:**
* File systems on computers.
* Organizational charts.

graph TD;
    Root[CEO] --> Manager1;
    Root[CEO] --> Manager2;
    Manager1 --> EmployeeA;
    Manager1 --> EmployeeB;
    Manager2 --> EmployeeC;
---
###2. Network Database Model
Concept: An extension of the hierarchical model that allows for more flexible relationships. Data is organized as a graph rather than a tree.

Structure: Graph structure.

Relationship: Many-to-Many (M:N).

Flexibility: A child record can have multiple parents.

Example:

Telecom networks: Managing connections between various nodes.

Transport systems: Routes connecting multiple cities.

Code snippet
graph TD;
    StoreA --> Product1[Laptop];
    StoreA --> Product2[Phone];
    StoreB --> Product1;
    StoreB --> Product2;
    VendorX --> StoreA;
    VendorY --> StoreB;
---
3. Relational Database Model (RDBMS)
Concept: The most widely used model today. Data is stored in structured tables (relations) which are linked by common data elements (keys).

Tables: Called Relations.

Rows: Called Tuples (represent a single record).

Columns: Called Attributes (represent properties of the data).

Examples: MySQL, Microsoft SQL Server, PostgreSQL.

Code snippet
erDiagram
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER {
        int id PK
        string name
        string email
    }
    ORDER {
        int order_id PK
        int customer_id FK
        date order_date
    }
---
###4. Object-Oriented Database Model (OODBMS)
Concept: Data is represented in the form of objects, similar to Object-Oriented Programming (OOP). This is ideal for handling complex data structures that don't fit well into rows and columns.

Key Features: Supports Classes, Objects, Inheritance, Encapsulation, and Polymorphism.

Use Cases: Multimedia files, graphics, scientific simulations, CAD (Computer-Aided Design).

Examples: ObjectDB, db4o.

---

###5. Object-Relational Database Model (ORDBMS)
Concept: A hybrid model that builds upon the relational model by adding object-oriented features. Data is still stored in tables, but the database supports complex data types and methods.

Structure: Table-based but with object capabilities.

Advantages: Combines the scalability of RDBMS with the flexibility of OODBMS.

Examples: PostgreSQL, Oracle Database.

---
###☁️ Cloud Database
Concept: A database that runs on a cloud computing platform. It provides database services over the internet, offering high flexibility and scalability without the need for physical hardware management.

Benefits:

Scalability: Easily scale storage and compute power up or down.

Accessibility: Access data from anywhere via the internet.

Cost-Effective: Pay-as-you-go models.

Examples:

Amazon Web Services (AWS): Amazon RDS, DynamoDB.

Google Cloud Platform (GCP): Cloud SQL, Firestore.

Microsoft Azur
---
###🚀 NoSQL DBMS (Not Only SQL)
Concept: Designed to handle massive volumes of data, specifically unstructured or semi-structured data (Big Data). Unlike RDBMS, NoSQL databases do not use a fixed tabular schema.

Key Features:

High Performance: Optimized for specific data models and access patterns.

Scalability: Designed for horizontal scaling (adding more servers).

Flexibility: Dynamic schemas allow for unstructured data storage.

Types of NoSQL Databases:

Key-Value Stores: (e.g., Redis)

Document Stores: (e.g., MongoDB)

Column-Family Stores: (e.g., Cassandra)

Graph Databases: (e.g., Neo4j)

Code snippet
mindmap
  root((NoSQL Types))
    Key-Value
      Redis
      DynamoDB
    Document
      MongoDB
      CouchDB
    Column-Family
      Cassandra
      HBase
    Graph
      Neo4j
      Amazon Neptune
⚡ ACID Properties
To ensure data integrity, reliable transactions in a DBMS must adhere to ACID properties:

Atomicity: The entire transaction takes place at once or doesn't happen at all.

Consistency: The database must remain in a consistent state before and after the transaction.

Isolation: Multiple transactions occur independently without interference.

Durability: The changes of a successful transaction are saved permanently, even in the event of a system failure.

🤝 Contributing
Contributions, issues, and feature requests are welcome!

📝 License
This project is MIT licensed.
