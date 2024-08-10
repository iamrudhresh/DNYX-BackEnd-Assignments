
# Backend Assignment 3: Integrating Prisma with Express for CRUD Operations

## Prisma Setup

- Install Prisma: `npm install @prisma/cli @prisma/client`
- Configure `.env` with PostgreSQL database connection URL Using NEON DB.

## Define Data Models

```prisma
model User {
  id        Int      @id @default(autoincrement())
  name      String
  email     String   @unique
  createdAt DateTime @default(now())
}
```

```prisma
model Post {
  id        Int      @id @default(autoincrement())
  title     String
  content   String
  createdAt DateTime @default(now())
}
```

- Create `schema.prisma` with User and Post models.
- Run Prisma migrations: `npx prisma migrate dev --name init`

## Express Routes with Prisma

- Update Express server to use Prisma for CRUD operations.
- Implement routes for CRUD operations.

## Testing

- Use Postman to test CRUD routes.
- Verify database changes in PostgreSQL database on Neon DB.

## Submission Guidelines

- Submit source code including `schema.prisma`, `index.js`, `.env`, etc.
- Provide setup instructions and CRUD operations guide in README.md.
- Include screenshots/videos of testing with Postman and database changes verification.
