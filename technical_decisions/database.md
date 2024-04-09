---
title: Database Options
layout: default
parent: Technical decisions
nav_order: 2
---

The main decision we had to make in regards to our database was between SQL and NoSQL. Our aim for 'Neighbourhood' was to allow users to connect and and be able to help each other in an inutitive way, thus we needed a robust database solution capable of handling complex data relationships while also being easy to adapt as our requirements changed.

After evaluating various database options, including popular NoSQL databases like MongoDB, we ultimately decided to adopt PostgreSQL with Prisma due to the following reasons:

**1. Data Integrity and Structure:**
PostgreSQL's adherence to the SQL standard provided us with a solid foundation for maintaining data integrity and enforcing relationships between different data entities.

**2. Flexible Data Modeling:**
While SQL databases are traditionally associated with rigid schemas, Prisma offered us the flexibility to adapt our data model on-the-fly without sacrificing the benefits of relational databases. This allowed us to iterate quickly during the development phase and accommodate evolving user requirements seamlessly.

**3. Performance and Scalability:**
Despite the perception that NoSQL databases excel in scalability, PostgreSQL—with its support for advanced indexing, query optimization, and transaction management—proved to be a formidable contender. Coupled with Prisma's efficient query builder and real-time data synchronization capabilities, we were confident in our ability to scale our infrastructure to meet growing demand.

**4. Developer Productivity:**
Prisma's intuitive API and auto-generated query builder significantly accelerated our development process, allowing our team to focus on implementing features rather than wrestling with database configurations or writing complex SQL queries.

By leveraging PostgreSQL with Prisma as our database solution, we successfully launched 'Neighbourhood', and exceeded our expectations in terms of performance, reliability, and scalability. Overall we are very satisfied with the decision we made in regards to working with PSQL and Prisma.
