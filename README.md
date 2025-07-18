# Express.js PostgreSQL CRUD API

## Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Set up PostgreSQL database:**
   - Make sure you have PostgreSQL running.
   - Create a database (default: `postgres`).
   - Create the `users` table:
     ```sql
     CREATE TABLE users (
       id SERIAL PRIMARY KEY,
       name VARCHAR(100),
       email VARCHAR(100),
       age INTEGER
     );
     ```

3. **Configure environment variables (optional):**
   - By default, the app connects to PostgreSQL with:
     - user: `postgres`
     - password: `postgres`
     - host: `localhost`
     - port: `5432`
     - database: `postgres`
   - You can override these by setting `PGUSER`, `PGPASSWORD`, `PGHOST`, `PGPORT`, and `PGDATABASE`.

4. **Start the server:**
   ```bash
   node index.js
   ```

## API Endpoints

- `GET /users` - Get all users
- `GET /users/:id` - Get a specific user
- `POST /users` - Create a new user
  - JSON body: `{ "name": "Name", "email": "email@example.com", "age": 30 }`
- `PUT /users/:id` - Update a user
  - JSON body: `{ "name": "Name", "email": "email@example.com", "age": 30 }`
- `DELETE /users/:id` - Delete a user

Server runs on [http://localhost:3000](http://localhost:3000) by default.