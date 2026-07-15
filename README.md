# CodeArena – Online Judge & Coding Practice Platform

CodeArena is a full-stack online judge and coding practice platform that supports real-time code evaluation, multi-language sandboxed execution, and AI-powered learning assistance.

## 🚀 Features

- **Real-time Code Evaluation** – Submit code and receive instant verdicts using a sandboxed multi-language execution engine.
- **Authentication & Authorization** – Secure JWT and bcrypt-based authentication with role-based access control (Admin & User roles).
- **Multi-language Code Execution** – Powered by the Judge0 API for sandboxed compilation and execution across multiple languages.
- **Custom Online Code Editor** – Integrated browser-based editor with AI-powered hints and video editorials to guide learning.
- **Optimized Backend** – 10+ RESTful APIs backed by MongoDB for persistence and Redis for caching, reducing average API response latency.
- **Production Deployment** – Backend deployed on AWS EC2 with a CI/CD pipeline for scalable, production-grade delivery.

## 🛠️ Tech Stack

| Layer            | Technology                     |
|------------------|---------------------------------|
| Frontend         | React.js                       |
| Backend          | Node.js, Express.js            |
| Database         | MongoDB                        |
| Caching          | Redis                          |
| Code Execution   | Judge0 API                     |
| Authentication   | JWT, bcrypt                    |
| AI Integration   | OpenAI API                     |
| Deployment       | AWS EC2, CI/CD                 |

## 📐 Architecture Overview

1. **Client (React.js)** – Provides the code editor UI, problem statements, submission history, and admin dashboard.
2. **API Layer (Node.js/Express.js)** – Exposes RESTful endpoints for authentication, problem management, and submissions.
3. **Execution Engine (Judge0 API)** – Executes submitted code in isolated sandboxes across multiple languages and returns verdicts.
4. **Data Layer (MongoDB + Redis)** – MongoDB handles persistent storage of users, problems, and submissions; Redis caches frequently accessed data to reduce latency.
5. **AI Layer (OpenAI API)** – Powers in-editor hints and assists users when they're stuck on a problem.

## 🔑 Key Highlights

- Role-based access control across 2 user roles (Admin, User).
- 10+ RESTful APIs designed for scalability and low latency.
- CI/CD pipeline enabling continuous, production-grade deployment on AWS EC2.
- AI-powered hints integrated directly into the coding workflow.

## 📦 Getting Started

### Prerequisites
- Node.js (v16+)
- MongoDB instance
- Redis instance
- Judge0 API access
- OpenAI API key

### Installation
```bash
# Clone the repository
git clone <repository-url>
cd codearena

# Install backend dependencies
cd server
npm install

# Install frontend dependencies
cd ../client
npm install
```

### Environment Variables
Create a `.env` file in the `server` directory with:
```
MONGO_URI=your_mongodb_connection_string
REDIS_URL=your_redis_connection_string
JWT_SECRET=your_jwt_secret
JUDGE0_API_KEY=your_judge0_api_key
OPENAI_API_KEY=your_openai_api_key
```

### Running the App
```bash
# Start backend
cd server
npm start

# Start frontend
cd ../client
npm start
```
