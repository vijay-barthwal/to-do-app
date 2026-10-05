# 📝 Todo App - Dockerized Full Stack Application

A full-stack Todo application fully containerized using Docker and Docker Compose.
Built as part of the 90DaysOfDevOps challenge - Day 36.

## 🏗️ Architecture
```
┌─────────────────────────────────────────────┐
│              Docker Network                  │
│                                             │
│  ┌──────────┐   ┌──────────┐   ┌─────────┐ │
│  │ Frontend │──▶│ Backend  │──▶│  MySQL  │ │
│  │  React   │   │ Node.js  │   │    DB   │ │
│  │ Port 3000│   │ Port 5000│   │ Port3306│ │
│  └──────────┘   └──────────┘   └─────────┘ │
└─────────────────────────────────────────────┘
```

## 🛠️ Tech Stack
- **Frontend**: React.js served via Nginx
- **Backend**: Node.js + Express.js REST API
- **Database**: MySQL 8
- **Containerization**: Docker + Docker Compose

## 📁 Project Structure
```
todo-app/
├── backend/
│   ├── Dockerfile
│   ├── index.js
│   └── package.json
├── frontend/
│   ├── Dockerfile
│   ├── public/
│   └── src/
├── mysql/
│   └── init.sql
└── docker-compose.yml
```

## 🐳 Docker Hub Images
- Frontend: `vijaybarthwal1/todo-frontend`
- Backend: `vijaybarthwal1/todo-backend`
- MySQL: `vijaybarthwal1/mysql-cont`

## 🚀 How to Run

### Prerequisites
- Docker
- Docker Compose

### Steps
```bash
# Clone the repo
git clone git@github.com:vijay-barthwal/to-do-app.git
cd to-do-app

# Start all services
docker-compose up -d

# Check running containers
docker ps
```

Open browser: **http://localhost:3000**

## 🔥 Features
- Add new todos
- Mark todos as complete
- Delete todos
- Data persists in MySQL database

## 📚 What I Learned
- Writing Dockerfiles for Node.js and React apps
- Multi-stage Docker builds to reduce image size
- Docker Compose for multi-container applications
- Container networking and service communication
- MySQL data persistence using Docker volumes
- Healthchecks for proper container startup order