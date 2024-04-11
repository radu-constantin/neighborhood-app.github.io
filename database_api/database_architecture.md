---
title: Database Architecture
layout: default
parent: Database and API
---

In the case of _Neighbourhood's_ development, the first thing that we started with was designing the database and identifying the main entities that interact with each other. Based on our requirements for the MVP, we came up with the following list:

- Neighbourhood
- User
- Request
- Response

We then fleshed out each entity by applying the concepts of database normalization as defined by E.F. Codd in his paper[^1]. Using these norms, we strived to reduce data redundancy and ensure data consistency.

![Neighborhood Model](../assets/images/db_model.png)

One of the most important aspects of our database is the fact that we leveraged the power and accesibility provided by ORM's (Object Relational Mapping), in our case Prisma. This greatly improved the speed of development while also providing the added benefit of type safety since Prisma automatically generated TypeScript types for all the entities in our database. Switching from writing SQL directly to using objects was a change that enabled us to achieve greater development speed and adaptability.

Even though we leveraged the advantages of ORM's, our initial schema was still developed in SQL, which we then converted to a Prisma schema file.
This schema met all of our requirements when we first started development, but as we decided to add more features such as real-time notifications and location based search, it also had to adapt in order to meet our growing needs. Thankfully, since our adoption of Prisma, all changes were easy to implement.

![Database ERD](../assets/images/neighborhood_erd.png)

---

[^1]: https://www.seas.upenn.edu/~zives/03f/cis550/codd.pdf
