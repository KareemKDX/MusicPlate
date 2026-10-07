# MusicPlate

MusicPlate is a simplified music streaming service inspired around the bigger music streaming services we have today, built as a school project.

## Features

- Start page with a selection of songs that anyone can see without an account
- Registration and login with JWT
- Passwords are hashed with bcrypt
- Profile page where users can see their subscription and change plan
- Three subscription plans with different limits (number of playlists, early access)
- Create and manage your own playlists
- Responsive design for both desktop and mobile

## Tech stack

- Frontend: React, TypeScript, React Router, Axios
- Backend: Node.js, Express, TypeScript
- Database: PostgreSQL
- Authentication: JWT and bcryptjs
- Hosted on render

## Getting started

1. Clone the project

```bash
git clone <repo-url>
```

2. Install dependencies in both the frontend and backend folders

```bash
npm install
```

3. Create a `.env` file in the backend folder

```
DATABASE_URL=your-database-url
JWT_SECRET=any-secret-key
```

The frontend also needs a `.env` file:

```
VITE_API_URL=http://localhost:4001
```

4. Start the backend (runs on port 4001)

```bash
npm run dev
```

5. Start the frontend in a new terminal

```bash
npm run dev
```

## API

| Method | Route | Description | Requires login |
|--------|-------|-------------|----------------|
| POST | /auth/register | Create account | No |
| POST | /auth/login | Log in | No |
| GET | /api/songs | Get all songs | No |
| GET | /api/subscriptions | Get all plans | No |
| GET | /api/profile | Get your profile | Yes |
| PATCH | /api/profile/subscription | Change plan | Yes |

