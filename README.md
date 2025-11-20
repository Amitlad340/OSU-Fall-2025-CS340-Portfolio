# Coffee Explorers – Project Documentation (CS340)

This repository contains the official documentation for **Coffee Explorers**, a full-stack database project completed for CS340 (Introduction to Databases) at Oregon State University.

 **No source code is included** 
This repo showcases the design work, SQL development, PL/SQL logic, database architecture, and problem-solving that went into building the project.

---

## Collaboration

This project was completed collaboratively by:

- Amit Lad
- Viggo Larson

We worked together on designing the schema, implementing SQL/PL-SQL logic, building routes for CRUD operations, and validating data integrity throughout the app.

---

## Project Overview

Coffee Explorers is a database-driven web application that allows users to manage:

- Customer accounts  
- Coffee products  
- Orders  
- Payment methods  
- Many-to-many relationships using a junction table (`OrdersCoffees`)

The application uses a Node.js + Express backend with a MariaDB relational database, performing real-time CRUD operations through a web interface.

---

## Skills Demonstrated

###  SQL Development (MariaDB)
- Complex SELECT queries using joins, subqueries, and filtering  
- INSERT/UPDATE/DELETE operations with data validation  
- Use of row-count logic, safe updates, and explicit transaction handling  
- Joined displays (e.g., show customer names with each order or payment method)  

### Stored Procedures & PL/SQL Logic
- Procedures for:
  - Deleting customers safely  
  - Updating counts and totals  
  - Cascaded deletes across foreign keys  
  - Transaction-protected operations  
- Error handling using:
  - `DECLARE ... HANDLER`  
  - `SIGNAL` / custom messages  
  - `START TRANSACTION ... COMMIT/ROLLBACK`  
- Defensive coding against invalid input  
- Conditional logic (IF/ELSE, ROW_COUNT checks)

### Relational Database Design**
- ERD development showing:
  - 1:Many (Customers → Orders)
  - 1:Many (Customers → Payment Methods)
  - M:Many (Orders ↔ Coffees using OrdersCoffees)
- Proper primary/foreign key selection  
- Preventing orphan records with `ON DELETE CASCADE` / `SET NULL` strategies  
- Normalization through 3NF to eliminate redundancy  
- Clean junction table design for many-to-many ordering  

### Performance & Optimization**
- Reduced redundant queries using proper join strategies  
- Ensured efficient table scans through good indexing  
- Used numeric foreign keys rather than expensive text lookups  
- Removed unnecessary nested queries  
- Designed tables to minimize update cost and improve referential integrity  

### Backend Integration (Node.js + Express)**
- RESTful routing for CRUD operations  
- Handlebars pages dynamically rendering SQL query results  
- Input validation before database calls  
- Modular route files (create, update, delete)  
- Connected SQL logic to web forms for real-time updates  

---

## 📄 Documentation

All diagrams, stored procedures, queries, schema definitions, screenshots, and explanations are provided in the PDF below:
