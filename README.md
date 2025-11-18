

## Setup Instructions

### 1. Install Dependencies

```bash
npm install
```

### 2. Database Setup

1. Make sure MySQL is installed and running
2. Create a database (or use the schema.sql file):
   ```bash
   mysql -u root -p < database/schema.sql
   ```
   Or manually:
   ```sql
   CREATE DATABASE job_portal;
   USE job_portal;
   -- Then run the SQL from database/schema.sql
   ```

### 3. Environment Configuration

1. Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```

2. Update `.env` with your database credentials:
   ```env
   PORT=3000
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_password
   DB_NAME=job_portal
   DB_PORT=3306
   JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
   JWT_EXPIRE=7d
   ```

### 4. Run the Server

```bash
# Development mode (with nodemon)
npm run dev

# Production mode
npm start
```

The server will start on `http://localhost:3000` (or the port specified in `.env`).
