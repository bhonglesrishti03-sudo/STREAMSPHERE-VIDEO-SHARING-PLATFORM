# StreamSphere 🎥
### A Full-Stack Video-Sharing & Creator-Community Platform

StreamSphere is a full-stack web application built with the MERN stack that brings video sharing and creator-community interactions together in one platform. It includes a React frontend and a Node.js/Express backend, with MongoDB for data persistence and Cloudinary integration for media uploads.

The project explores core full-stack development concepts, including REST API design, authentication, database modeling, media handling, and frontend state management.

## ✨ Features

### 🔐 Authentication & User Management
- User registration and login workflows
- JWT-based authentication middleware
- Password hashing with bcrypt
- User profile and account-related operations
- Avatar and cover-image upload support in the backend

### 📹 Video Management
- Backend endpoints for video-related operations
- Video metadata and data models
- Cloudinary integration for media uploads
- Video-related API services in the frontend
- Video discovery and management capabilities supported by the implemented API


### 🎨 Frontend & State Management
- Component-based React architecture
- Client-side routing with React Router
- Centralized state management with Redux Toolkit
- State persistence with Redux Persist
- API communication using Axios
- Form handling with React Hook Form and Zod
- Tailwind CSS and reusable UI components
- Icons using Lucide React

*Note: The availability of individual features depends on backend configuration, frontend integration, and required environment variables. Verify each workflow before presenting it as production-ready.*

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | React 19, Vite, React Router |
| Styling | Tailwind CSS, reusable UI components |
| State Management | Redux Toolkit, React Redux, Redux Persist |
| API Communication | Axios |
| Forms & Validation | React Hook Form, Zod |
| Backend | Node.js, Express 5 |
| Database | MongoDB, Mongoose |
| Authentication | JSON Web Tokens (JWT), bcrypt |
| Media Handling | Multer, Cloudinary |
| Middleware | CORS, cookie-parser |
| Development Tools | Git, npm, ESLint |

## 🏗️ Project Architecture

The application is organized into separate frontend and backend projects.

```text
StreamSphere/
├── client/
│   ├── public/
│   ├── src/
│   │   ├── api/                  # API configuration
│   │   ├── components/           # Reusable UI components
│   │   ├── service/              # Frontend API services
│   │   └── ...                   # Pages, state and utilities
│   ├── package.json
│   └── vite.config.js
│
├── server/
│   ├── src/
│   │   ├── controller/            # Request handlers
│   │   ├── db/                    # Database connection
│   │   ├── middlewares/            # Authentication and uploads
│   │   ├── models/                 # Mongoose data models
│   │   ├── routes/                 # API route definitions
│   │   ├── utils/                  # Shared backend utilities
│   │   ├── app.js                  # Express configuration
│   │   └── index.js                # Server entry point
│   └── package.json
│
├── .gitignore
└── readme.md
```

## 🚀 Getting Started

### Prerequisites

Install or prepare the following:

- Node.js and npm
- MongoDB local instance or MongoDB Atlas connection
- Cloudinary account for cloud media functionality
- Git

### 1. Clone the repository

```bash
git clone https://github.com/bhonglesrishti03-sudo/STREAMSPHERE-VIDEO-SHARING-PLATFORM.git
cd STREAMSPHERE-VIDEO-SHARING-PLATFORM
```

### 2. Configure environment variables

Create the environment file or files expected by the backend and frontend. Check the source code for the exact variable names and locations before starting the application.

Backend configuration typically includes values such as:

```env
PORT=8000
CORS_ORIGIN=http://localhost:5173
MONGODB_URI=your_mongodb_connection_string

ACCESS_TOKEN_SECRET=your_access_token_secret
ACCESS_TOKEN_EXPIRY=1d
REFRESH_TOKEN_SECRET=your_refresh_token_secret
REFRESH_TOKEN_EXPIRY=10d

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

These are example settings, not a guarantee of the exact variable names used by every module. Match them to the existing implementation.

**Security:** Never commit `.env` files, database credentials, JWT secrets, or Cloudinary API secrets to GitHub.

### 3. Install backend dependencies

Open a terminal in the project root:

```bash
cd server
npm install
```

### 4. Install frontend dependencies

Open a second terminal in the project root:

```bash
cd client
npm install
```

### 5. Start the backend

From the `server` directory:

```bash
npm run dev
```

The backend requires a valid database connection and the environment variables expected by the source code.

### 6. Start the frontend

From the `client` directory:

```bash
npm run dev
```

Open the local URL displayed by Vite in your browser. The frontend API configuration must point to the running backend.

## 🔗 API Route Groups

The Express application mounts the following route groups under `/api/v1`:

| Resource | Base path |
|---|---|
| Users and authentication | `/api/v1/users` |
| Videos | `/api/v1/videos` |
| Subscriptions | `/api/v1/subscribe` |
| Comments | `/api/v1/comments` |
| Tweets / posts | `/api/v1/tweets` |
| Likes | `/api/v1/likes` |
| Playlists | `/api/v1/playlists` |

Refer to the corresponding files inside `server/src/routes/` for individual endpoints, HTTP methods, request parameters, and authentication requirements.

## 🗄️ Data Models

The backend contains Mongoose models for the following resources:

- Users
- Videos
- Comments
- Likes
- Subscriptions
- Playlists
- Tweets/posts

These models provide the data structures used by the backend controllers and route handlers.

## 🔒 Security & Media Handling

The backend includes several components intended to support secure application workflows:

- JWT authentication middleware for protected routes
- bcrypt for password hashing
- Cookie parsing for cookie-based request handling
- Multer middleware for handling file uploads
- Cloudinary utilities for uploading and deleting cloud media
- CORS configuration for controlling browser-based cross-origin access

The effectiveness of these protections depends on the configuration and implementation of each workflow.

## 🧪 Development & Build

To create a production frontend build:

```bash
cd client
npm run build
```

To run frontend lint checks:

```bash
npm run lint
```

To start the backend in development mode:

```bash
cd server
npm run dev
```

The backend package currently contains a placeholder test script; automated backend test coverage should not be assumed.

## 📚 Learning Outcomes

Working with this codebase provides exposure to:

- Designing RESTful APIs with Express
- Organizing controllers, routes, middleware, and models
- Connecting React frontend services to backend endpoints
- Working with MongoDB and Mongoose
- Implementing JWT-based authentication patterns
- Handling uploads with Multer and Cloudinary
- Managing client-side state with Redux Toolkit
- Configuring and running a full-stack JavaScript application

## 🤝 Credits & Attribution


Educational guidance: [Hitesh Choudhary](https://github.com/hiteshchoudhary) and [Chai aur Code](https://www.chaicode.com/).



**Built with the MERN stack — MongoDB, Express, React, and Node.js.**
