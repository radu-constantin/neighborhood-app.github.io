---
title: Database Architecture
layout: default
parent: Database and API
---

Our first priority when starting off was designing the database and identifying the main entities that would consist the pillars on which back- and front-end would be based off of. Based on our initial requirements for the MVP, we settled on the following:

- Neighbourhood
- User
- Request
- Response

We then fleshed out each entity by applying the concepts of database normalization, as defined by E.F. Codd in his paper[^1]. Using these norms, we strived to reduce data redundancy and ensure data consistency.

![Neighborhood Model](../assets/images/db_model.png)

One of the most important aspects of our database is the fact that we leveraged the power and accesibility provided by ORMs (Object Relational Mappers), in our case, Prisma. That significantly improved the speed of development, while also providing the added benefit of type safety since Prisma automatically generated TypeScript types for all the entities in our database. Switching from writing and executing complex SQL queries through [pg](https://www.npmjs.com/package/pg) to using objects was a change that enabled us to achieve greater development speed and adaptability.

Even though we took benefit of the advantages of an ORM, our initial schema was still developed in SQL, which we then converted to a Prisma schema file.
This schema met all of our requirements when we first started development, but as we decided to add more features, such as real-time notifications and location-based search, it also had to adapt to meet our growing needs. Thanks to our decision to incorporate Prisma, all those changes were fairly easy to implement.

![Database ERD](../assets/images/neighborhood_erd.png)

---

[^1]: https://www.seas.upenn.edu/~zives/03f/cis550/codd.pdf
