# My-Class-App
My-Class-App is a web application that helps schools manage courses, schedules, assignments, grades, and communications. It provides role-based access for **teachers**, **students**, and **parents**, enabling:
- Course and roster management
- Assignment creation, submission, and grading
- Calendar and schedule viewing
- Announcements and notifications
- Secure file uploads and downloads
- Basic analytics and progress tracking
## Tech stack
- Frontend: React (Vite)
- Backend: Node.js + Express
- Database: PostgreSQL
- File storage: Amazon S3 (or alternative object storage)
## Quick start
1. Copy the repository and create `backend/.env` with required secrets.
2. Run the database migrations: `psql $DATABASE_URL -f backend/src/db/migrations.sql`
3. Start services (local): `docker-compose up --build`
4. Seed sample data: `cd backend && node src/seed/seed.js`
5. Open the frontend at `http://localhost:5173` and the API at `http://localhost:4000/api`.
## Features to add next
- Parent accounts and permission controls
- In-app messaging between teachers and parents
- Attendance tracking
- Role-based dashboards and reports
- Mobile-friendly UI and accessibility improvements
## Security notes
- Use a strong `JWT_SECRET` and store secrets in a secure vault for production.
- Validate and sanitize all user input and uploaded files.
- Serve private files via signed URLs rather than public S3 links.
