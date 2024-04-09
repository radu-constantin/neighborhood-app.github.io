---
title: Database Architecture
layout: default
parent: Database and API
---

In the process of designing the database we identified the following main entities:

- Neighbourhood
- User
- Requests
- Responses

Based on these we've created the following initial schema:
![Database ERD](../assets/images/neighborhood_erd.png)

This schema met all of our requirements when we first started development, but as we've decided to add more features such as real-time notifications and location based search, the schema suffered some changes.
In the process of adapting the database to our growing needs, the decision to adopt Prisma saved us a lot of time. Prisma is an ORM (Object Relational Mapping) which maps the entities of a database to objects that allowed us to create, read and manipulate data. It hides some of the complexity of databases and allow for easier interaction with the data via objects.
