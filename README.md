# Project 2: To-Do List Application (React + Express + MongoDB)
Features: register/login with JWT, password hashing, task CRUD, status workflow, search, filtering, sorting, server-side pagination, validation, per-user task ownership, rate limiting.

## Windows setup
1. Install Node.js LTS and MongoDB Community Server (or use MongoDB Atlas).
2. Open `Todo-Application` in VS Code.
3. Run `npm install`.
4. Copy `.env.example` to `.env`; set a private random JWT_SECRET with at least 32 characters.
5. Start MongoDB if using local MongoDB.
6. Run `npm run dev`.
7. Open **http://localhost:5173**. Register an account, then add tasks. Backend runs on port 5001.

## REST APIs
- POST `/api/auth/register` JSON `{ "name":"Example User", "email":"user@example.com", "password":"aStrongPass123" }`
- POST `/api/auth/login` JSON `{ "email":"user@example.com", "password":"aStrongPass123" }`
- GET `/api/tasks?page=1&limit=6&status=Pending&search=study&sort=newest` (JWT Bearer token required)
- POST `/api/tasks` add task
- PATCH `/api/tasks/:id` edit task/status
- DELETE `/api/tasks/:id` delete task

Never commit `.env` or secrets. For public production, add HTTPS, secure token storage, tests, monitoring and deployment configuration.
