---
title: CI/CD
layout: default
parent: Challenges
---

One of the main challenges we faced while developing <span style="color:#FF0054">Neighbourhood</span> was creating a development pipeline that ensured the integrity of our application, without slowing down development.
These objectives transalted to the following requirements:

1. Quality test suites;
2. A reproducible test environment for the database;
3. A way to prevent merging code changes without approval and automatic test runs;

The first point was implemented by creating multiple suites of unit and integration tests that achieved a wide coverage over the codebase.

For our second objective, in order to prevent the tests from interfering with the development data, we used a Docker container that hosted two separate databases, one for development and one for testing purposes. We favoured hosting the databases in a container rather than having the whole team host their own database instance on their respective machines to avoid common 'it works on my machine' problems.

The third point was achieved by protecting the `main` branch with the aid of Github actions. We created a Github actions workflow that fired up the Docker container and our app and ran our tests. The workflow started every time a Pull Request was issued or updated. To successfully merge the PR, the tests in the workflow must all pass and the PR had to be reviewed and approved by at least one other contributor. Only when these 2 conditions were met, the PR could be merged into the `main` branch.

The final piece of the puzzle was automating the deployment pipeline. This was easily achieved by using [_Render_](https://render.com/) to deploy both the backend and the frontend. _Render_ had the main advantage of automatically deploying when an update was detected on the specified branch (in our case `main`).

By implementing all the above steps, we built a completely automated pipeline that took our code from development to production while ensuring the integrity of our codebase.
