🗄️ Database Management Systems (DBMS)
📖 Introduction

A Database Management System (DBMS) is software designed to store, manage, retrieve, and organize data efficiently.
It acts as an interface between users/applications and the database, ensuring data is consistently structured, secure, and easily accessible.

🎯 Key Objectives of DBMS

✅ Reduce Redundancy – Minimizes duplicate data through centralized control.
✅ Ensure Consistency – Maintains data integrity across the system.
✅ Data Access & Management – Supports concurrent access, transactions, and recovery.
✅ Security – Protects data from unauthorized access.
✅ Data Integrity – Enforces rules and constraints for accurate data.

🗂️ Types of Database Models
1️⃣ Hierarchical Database Model

Concept: Data organized in a tree-like parent–child structure

Structure: Tree

Relationship: One-to-Many (1:N)

Constraint: Each child has exactly one parent

Examples: File systems, organizational charts

graph TD;
    CEO --> Manager1;
    CEO --> Manager2;
    Manager1 --> EmployeeA;
    Manager1 --> EmployeeB;
    Manager2 --> EmployeeC;

2️⃣ Network Database Model

Concept: Extension of hierarchical model allowing multiple parent relationships

Structure: Graph

Relationship: Many-to-Many (M:N)

Flexibility: A child can have multiple parents

Examples: Telecom networks, transportation systems

graph TD;
    StoreA --> Laptop;
    StoreA --> Phone;
    StoreB --> Laptop;
    StoreB --> Phone;
    VendorX --> StoreA;
    VendorY --> StoreB;

3️⃣ Relational Database Model (RDBMS)

Concept: Most widely used model with data stored in tables

Rows: Tuples (records)

Columns: Attributes (fields)

Keys: Primary Key (PK), Foreign Key (FK)

Popular RDBMS Systems:

MySQL

PostgreSQL

Microsoft SQL Server

Oracle Database

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

4️⃣ Object-Oriented Database Model (OODBMS)

Concept: Data stored as objects similar to OOP

Features: Classes, inheritance, encapsulation, polymorphism

Use Cases: Multimedia, CAD, scientific simulations

Examples:

ObjectDB

db4o

5️⃣ Object-Relational Database Model (ORDBMS)

Hybrid of relational and object-oriented approaches

Supports complex data types and user-defined methods

Examples: PostgreSQL, Oracle Database

☁️ Cloud Databases

Databases hosted on cloud platforms with managed services.

Benefits

✔ Scalability
✔ Global accessibility
✔ Cost efficiency
✔ Automated backups

Major Cloud Providers

Amazon Web Services

AWS

Amazon RDS

DynamoDB

Google Cloud Platform

GCP

Cloud SQL

Firestore

Microsoft Azure

Azure

Azure SQL Database

🚀 NoSQL Databases

Designed for large-scale unstructured or semi-structured data.

Key Features

✔ High performance
✔ Horizontal scalability
✔ Flexible schema

Types of NoSQL Databases
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


Examples by Category

Key-Value → Redis

Document → MongoDB, CouchDB

Column-Family → Cassandra, HBase

Graph → Neo4j, Amazon Neptune

⚡ ACID Properties
Property	Meaning
Atomicity	Transaction completes fully or not at all
Consistency	Database remains valid before and after transaction
Isolation	Transactions execute independently
Durability	Committed changes are permanent
📌 ER Model Concept

The Entity–Relationship (ER) Model is a conceptual framework used to represent data and relationships in a database.

Purpose

✔ Models real-world objects
✔ Simplifies database design
✔ Easy visualization of relationships
✔ Standard representation of schema

🔑 Components of an ER Diagram
Component	Description	Symbol
Entities	Real-world objects	Rectangle
Attributes	Characteristics of entities	Ellipse
Relationships	Associations between entities	Diamond
Lines	Connect elements	Line
🏷️ Types of Entities

Strong Entity → Independent

Weak Entity → Depends on strong entity

🏷️ Types of Attributes

Single-valued

Multi-valued

Derived

Composite
