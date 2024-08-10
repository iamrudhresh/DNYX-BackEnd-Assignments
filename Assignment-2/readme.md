# Backend Assignment 2: Fetching Data from Neon DB using Prisma

## Prisma Setup
- Install Prisma: `npm install @prisma/cli @prisma/client`
- Configure `.env` with Neon DB PostgreSQL database connection URL.

## Define User Data Model
- Create `schema.prisma` with User model.

# User Data Model Schema

```prisma
model User {
  id        Int      @id @default(autoincrement())
  name      String
  email     String   @unique
  createdAt DateTime @default(now())
}
```
- Run Prisma migrations: `npx prisma migrate dev --name init`

## Express Route to Get User Data
- Update Express server to use Prisma for fetching user data.
- Implement `/api/users` route to fetch user data using Prisma.

## Testing
- Use Postman to test the `/api/users` route.
- Verify fetched user data from the Neon DB.

## Submission Guidelines
- Submit your project source code (`index.js`, `package.json`, etc.) Via Github Link.
- Include screenshots/videos of testing with Postman and verifying fetched data.
