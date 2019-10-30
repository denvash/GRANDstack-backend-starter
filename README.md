# [GRAND-Stack Backend Starter](https://grandstack.io/)

![GRANDstack](https://grandstack.io/docs/assets/img/grandstack_architecture.png)

## Features

- Backend as micro-service.
- Empowered version of [`grand-stack-stater`](https://github.com/grand-stack/grand-stack-starter) (`/api`)
- Linters - `eslint` & `prettier` configured
- Optional-Chaining

## Usage

Follow the official [GRANDstack Starter guide](https://grandstack.io/docs/getting-started-grand-stack-starter.html) for configuring Neo4j instance, you should also check the [Tutorial video](https://www.youtube.com/watch?v=rPC71lUhK_I).

> **TL;DR**: Initialize a DB instance and edit `.env` file, add secrets to `now` for deployment.

[![Deploy to now](https://deploy.now.sh/static/button.svg)](https://deploy.now.sh/?repo=https://github.com/social-gissy-network/core&env=NEO4J_USER&env=NEO4J_URI&env=NEO4J_PASSWORD)

1. Install Dependencies

   ```sh
   yarn install
   ```

2. Development

   ```sh
   yarn develop
   # Run for seeding the Neo4j DB
   yarn seed
   ```

3. Deployment

   ```sh
   npm i -g now
   now login
   ```

   Add secrets for Neo4j instance:

   ```sh
   now secret add neo4j_uri bolt://<YOUR_NEO4J_INSTANCE_HERE>
   now secret add neo4j_user <YOUR_DATABASE_USERNAME_HERE>
   now secret add neo4j_password <YOUR_DATABASE_USER_PASSWORD_HERE>
   ```

   [Integrate with Github](https://zeit.co/github) and deploy:

   ```sh
   now
   ```
