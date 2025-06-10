# Prisma ORM Summary

Prisma is a modern Object-Relational Mapping (ORM) tool designed for Node.js and TypeScript, enabling developers to interact with databases through an object-oriented approach.

## Defination of ORM

ORM (Object-Relational Mapping) allows developers to work with database records as objects, avoiding raw SQL queries. Popular ORMs include:
- *SQLAlchemy* (Python)
- *Sequelize* (JavaScript)
- *Hibernate* (Java)
- *Prisma*
- *Drizzle*

## Benefits of Using Prisma
-  Productivity: Reduces boilerplate code for database interactions.
-  Portability: Simplifies switching between different database systems.
-  Security: Prevents SQL injection attacks through parameterized queries.
-  Maintenance: Eases management of database schema changes.

### Getting started on Prisma
1. *Installation of Prisma*:
  ``` bash
   npm install prisma -D
   ```
   or
  ``` bash
   npm install prisma --save-dev
   ```

2. *Setting Up Prisma Project*:
   ```bash
   npx prisma init --datasource-provider postgresql
   ```

3. *Creating Your Model(s)* in schema.prisma.

4. *Run Migrations*:
   ```bash
   npx prisma migrate dev --name MIGRATION-NAME
  ``` 
5.  *Generate the Client*:
   ``` bash
   npx prisma generate
  ```  

### Defining Models

Models represent tables in the database and consist of fields corresponding to columns. Key concepts include:
-  Data Models
-  Field Types (e.g., String, Int)
-  Relations
-  Attributes (e.g., @id, @default)

## Migrations
These manage changes to your database schema using migrations. Create a migration after modifying your schema.prisma file:
```bash
npx prisma migrate dev --name initial-migration
```

## Prisma Client
The Prisma Client is a type-safe client for interacting with your database, supporting CRUD operations, filtering, and pagination.

### CRUD Operations
- *Create*: Adding new records to the database.

- *Read*: Retrieving required records.

- *Update*: Modifying the existing records.

- *Delete*: Removing records.


### Example CRUD Operations
- Create a Single Record
![insert](/images/insert.jpg)

- Read All Records:
![select](/images/select.jpg)

- Update a Record
![update](/images/update.jpg)

- Delete a Record
![delete](/images/delete.jpg)


## Relationships
Prisma supports defining relationships between models:

-  One-to-One: One record in one table corresponds to one record in another.
In the example, there is a one-to-one relation between *user* and *profile*
![one](/images/one.jpg)

In one-to-one relation;
- a user can have zero or one profile (*profile* field is optional on *user*)
- a profile must always be connected to one user


-  One-to-Many: One record in one table corresponds to multiple records in another.
In the example, there is one-to-many relation between *user* and *post* models
![many](/images/many.jpg)

In one-to-many relation;
- a user can have zero or more posts
- a post must always have an author

- Many-to-Many: Multiple records in one table correspond to multiple records in another.
