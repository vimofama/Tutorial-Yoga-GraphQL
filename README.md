# Yoga - GraphQL

Tutorial: [How to build a GrphQL server↗](https://the-guild.dev/graphql/yoga-server/tutorial/basic)

## Overview
---
GraphQL is the rising star of backend technologies. It’s a popular alternative for REST as an API design paradigm and is becoming the new standard for exposing the data and functionality of a web server.

In this tutorial, you’ll learn how to build a GraphQL HTTP server entirely from scratch.

You are going to use the following technologies:

- [Node.js↗](https://nodejs.org/)  - as an engine and runtime for our server

- [TypeScript↗](https://typescriptlang.org/)  - a strongly typed programming language that builds on JavaScript giving you better tooling at any scale

- graphql-yoga- the easiest way to build an HTTP GraphQL server

- [graphql-js↗](https://github.com/graphql/graphql-js) - we will use the core graphql library as execution engine for our server

- [GraphiQL↗](https://github.com/graphql/graphiql) : A graphical interface that allows you to interactively explore the functionality of a GraphQL API by sending query, mutation and subscription operations. It’s somewhat similar to [Postman↗](https://getpostman.com/) which offers comparable functionality for REST APIs. Among other things, GraphiQL:
    * Auto-generates comprehensive documentation for all available API operations
    * Provides an editor where you can write queries, mutations & subscriptions with auto-complete and syntax highlighting

- [SQLite↗](https://sqlite.org/) : A lightweight and easy-to-use relational database management system for persisting data on the file system

- [Prisma↗](https://prisma.io/) : The glue between your code and SQLite database. Use Prisma Client to access your database inside GraphQL resolvers

💡You can find the [code of the tutorial in this repository↗](https://github.com/dotansimha/graphql-yoga/tree/main/examples/hackernews)  or a step by step solution, with a commit for each step, on [this repository↗](https://github.com/Urigo/hackernews-node-ts) 

---
## Installation Guide

Follow these steps to get started with the project:

### 1. Clone the Repository

First, clone this repository to your local machine:
```bash
git clone https://github.com/vimofama/Tutorial-Yoga-GraphQL.git
```

### 2. Install Dependencies
Use `pnpm` to install all necessary dependencies:
```bash
pnpm install
```

### 3. Set Up the Database with Prisma
Generate the migrations for your database:
```bash
pnpm prisma migrate dev
```

If you make changes on `schema.prisma` file, you'll need to create a new migration:
```bash
pnpm prisma migrate dev --name name_of_migration
```
Then, generate new Prisma client:
```bash
pnpm prisma generate
```
---
## Running the Server
### Development Mode
To start the server in development mode, run the following command:
```bash
pnpm dev
```
### Production Mode
To start the server in production, use:
```bash
pnpm start
```
By default, the server will run on port `4000`.

---

## Additional Notes
* If you ever need to "reset" the database or clear migrations, you can run:
```bash
pnpm prisma migrate reset
```