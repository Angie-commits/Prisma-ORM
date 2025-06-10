# Prisma ORM Summarization

Prisma is a modern Object-Relational Mapping (ORM) tool designed for Node.js and TypeScript, enabling developers to interact with databases through an object-oriented approach.

## What is ORM?

ORM (Object-Relational Mapping) allows developers to work with database records as objects, avoiding raw SQL queries. Popular ORMs include:
- *SQLAlchemy* (Python)
- *Sequelize* (JavaScript)
- *Hibernate* (Java)
- *Prisma*
- *Drizzle*

## Benefits of Using Prisma
- *Productivity*: Reduces boilerplate code for database interactions.
- *Portability*: Simplifies switching between different database systems.
- *Security*: Prevents SQL injection attacks through parameterized queries.
- *Maintenance*: Eases management of database schema changes.

### Steps to Use Prisma
1. *Install Prisma*:
  ``` bash
   npm install prisma -D
   ```
   or
  ``` bash
   npm install prisma --save-dev
   ```

2. *Set Up Prisma Project*:
   ```bash
   npx prisma init --datasource-provider postgresql
   ```

3. *Create Your Model(s)* in schema.prisma.

4. *Run Migrations*:
   ```bash
   npx prisma migrate dev --name MIGRATION-NAME
  ``` 

5. *Generate the Client*:
  ``` bash
   npx prisma generate
 ```  

### Defining Models
Models represent tables in the database and consist of fields corresponding to columns. Key concepts include:
- *Data Models*
- *Field Types* (e.g., String, Int)
- *Relations*
- *Attributes* (e.g., @id, @default)

## Migrations
Manage changes to your database schema using migrations. Create a migration after modifying your schema.prisma file:
```bash
npx prisma migrate dev --name initial-migration
```

## Prisma Client
The Prisma Client is a type-safe client for interacting with your database, supporting CRUD operations, filtering, and pagination.

### CRUD Operations
- *Create*: Add new records to the database.
- *Read*: Retrieve records.
- *Update*: Modify existing records.
- *Delete*: Remove records.

### Example CRUD Operations
- *Create a Single Record*:
- *Read All Records*:
- *Update a Record*:
- *Delete a Record*:

## Relationships
Prisma supports defining relationships between models:
- *One-to-One*: One record in one table corresponds to one record in another.
- *One-to-Many*: One record in one table corresponds to multiple records in another.
- *Many-to-Many*: Multiple records in one table correspond to multiple records in another.

### Example One-to-One Relationship


### Example One-to-Many Relationship