# TaskFlow — Full-Stack Task Management Application

**TaskFlow** is a full-stack task management application built with the MERN stack. It helps individuals and teams organize work, assign responsibilities, manage deadlines, and monitor task progress through a clean, interactive dashboard.

**Developed and maintained by:** Divyanshu Kumar  
**Repository:** [github.com/divyanshu7077/TaskFlow](https://github.com/divyanshu7077/TaskFlow)  
**Live application:** [task-flow-sigma-lemon.vercel.app](https://task-flow-sigma-lemon.vercel.app/)

## Features

- **User authentication:** Sign up and log in using JWT-based authentication, with passwords hashed using bcrypt.
- **Task management:** Create, edit, delete, prioritize, and categorize tasks; optionally set due dates.
- **Workflow tracking:** Organize tasks across **Backlog**, **To-Do**, **In Progress**, and **Done** stages.
- **Team collaboration:** Add board members, assign tasks to members, and share tasks through read-only public access.
- **Task analytics:** View task progress and filter tasks by **Today**, **This Week**, or **This Month**.
- **Visual status indicators:** Highlight overdue and completed tasks for easier tracking.
- **Profile management:** Update account details, including name, email, and password.
- **Interactive interface:** Redux Toolkit state management, client-side routing, and toast notifications.

## Tech Stack

| Layer | Technologies |
| --- | --- |
| Frontend | React.js, Vite, React Router, Redux Toolkit, CSS |
| Backend | Node.js, Express.js, REST APIs |
| Database | MongoDB, Mongoose |
| Authentication & Security | JWT, bcrypt.js, CORS |
| Additional tools | Git, GitHub, npm, ESLint, React Toastify |

## Project Structure

```text
TaskFlow/
├── backend/             # Express server, API routes, database integration
├── frontend/            # React application and UI components
├── LICENSE
└── Readme.md
```

## Getting Started

### Prerequisites

- Node.js and npm
- MongoDB running locally or a MongoDB connection URI

### 1. Clone the repository

```bash
git clone https://github.com/divyanshu7077/TaskFlow.git
cd TaskFlow
```

### 2. Configure and run the backend

```bash
cd backend
npm install
```

Create a `.env` file inside `backend/`:

```dotenv
MONGODB_URI=mongodb://127.0.0.1:27017/task_management
FRONTEND_URL=http://localhost:5173
PORT=9000
JWT_SECRET=replace_with_a_long_random_secret
```

Start the development server:

```bash
npm run dev
```

### 3. Configure and run the frontend

Open a second terminal from the repository root:

```bash
cd frontend
npm install
```

Create a `.env` file inside `frontend/`:

```dotenv
VITE_BACKEND_URL=http://localhost:9000
VITE_FRONTEND_URL=http://localhost:5173
```

Start the frontend:

```bash
npm run dev
```

Open **http://localhost:5173** in your browser.

> **Security:** Never commit real `.env` files, database credentials, or JWT secrets to GitHub. Generate a strong, unique secret for each environment.

## Available Scripts

| Directory | Command | Purpose |
| --- | --- | --- |
| `frontend/` | `npm run dev` | Start frontend development server |
| `frontend/` | `npm run build` | Build frontend for production |
| `frontend/` | `npm run lint` | Check frontend code |
| `frontend/` | `npm run preview` | Preview production build |
| `backend/` | `npm run dev` | Start backend in development mode |
| `backend/` | `npm run start` | Start backend application |

## How It Works

1. A user signs up or logs in and receives an authentication token.
2. The React frontend sends requests to the Express backend through REST APIs.
3. The backend validates protected requests and interacts with MongoDB using Mongoose.
4. Users create and update tasks, move them between workflow stages, and view their progress in the dashboard.
5. Redux Toolkit manages application state and keeps the interface responsive to user actions.

## Developer

**Divyanshu Kumar**  
[GitHub](https://github.com/divyanshu7077) · [Email](mailto:dk7061607@gmail.com)

## License and Attribution

This repository includes an [MIT license](LICENSE). Any existing copyright and attribution notices in the license must be retained for material covered by them. If any third-party code is included, preserve its applicable attribution and license terms.
