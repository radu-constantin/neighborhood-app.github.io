---
title: CI/CD
layout: default
parent: Challenges
---

One of the main challenges that we were confronted with while developing _Neighbourhood_ was to create a development pipeline that ensured the integrity of our application, without slowing down development.
In order to achieve this objectives we had to implement the following:

1. Quality test suites;
2. A reproducible test environment for the database;
3. A way to prevent merging code changes without approval and automatic test runs;

The first point was achieved by creating multiple suits of unit and integration tests that achieved a wide coverage of our codebase. In order not to let the tests interfere with the development data, we used a Docker container that hosts two separate databases, one for development and one for testing purposes. We prefered hosting the databases in a container rather than having the whole team host their own database instance on their respective machines in order to avoid problems such as the common 'works on my machine'.

The third point was achieved by protecting the `main` branch with the aid of Github actions. We created a Github actions workflow that fired up the Docker container and our app and ran our tests. The workflow started every time a Pull Request was issued or updated. In order to be able to successfully merge the PR, the tests in the workflow must all pass and the PR must be reviewed and approved by another teammate. Only when these 2 conditions are met, the PR can be merged to the `main` branch.

The final piece of the puzzle was automating the deployment pipeline. This was easily achieved by using _Render_ to deploy both the backend and the frontend. _Render_ had the main advantage of automatically deploying when an update was detected on the specified branch (in our case `main`).

By leveraging all the steps above we have built a completely automated pipeline that took our code from development to production while ensuring the integrity of our codebase.
