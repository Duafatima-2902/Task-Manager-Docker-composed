# Task Manager Application

A simple task management application built with React frontend and Node.js/Express backend, containerized with Docker.

## Features

- ✅ Add new tasks with title and description
- ✅ Mark tasks as complete/incomplete
- ✅ Delete tasks
- ✅ Responsive design
- ✅ Real-time updates
- ✅ Docker containerization

## Project Structure

```
├── backend/           # Node.js/Express API
│   ├── package.json
│   ├── server.js
│   └── Dockerfile
├── frontend/          # React application
│   ├── package.json
│   ├── src/
│   │   ├── App.js
│   │   ├── App.css
│   │   ├── index.js
│   │   └── index.css
│   ├── public/
│   │   └── index.html
│   └── Dockerfile
├── docker-compose.yml # Docker orchestration
└── README.md
```

## Quick Start

### Prerequisites

- Docker
- Docker Compose

### Running the Application

1. **Clone or download this project**

2. **Run with Docker Compose:**
   ```bash
   docker-compose up --build
   ```

3. **Access the application:**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000
   - Health Check: http://localhost:5000/health

### Development Commands

```bash
# Build and start services
docker-compose up --build

# Run in detached mode
docker-compose up -d

# Stop services
docker-compose down

# View logs
docker-compose logs

# Rebuild specific service
docker-compose up --build backend
```

## API Endpoints

- `GET /api/tasks` - Get all tasks
- `GET /api/tasks/:id` - Get a specific task
- `POST /api/tasks` - Create a new task
- `PUT /api/tasks/:id` - Update a task
- `DELETE /api/tasks/:id` - Delete a task
- `GET /health` - Health check

## Technologies Used

### Backend
- Node.js
- Express.js
- CORS middleware
- Body-parser

### Frontend
- React 18
- Axios for API calls
- CSS3 with modern styling
- Responsive design

### DevOps
- Docker
- Docker Compose
- Multi-stage builds
- Health checks

## Default Tasks

The application comes with some sample tasks:
1. Learn Docker
2. Build Task Manager
3. Deploy Application

## Notes

- The backend uses in-memory storage (tasks reset on restart)
- For production, consider adding a database (PostgreSQL, MongoDB, etc.)
- The frontend is built for production and served with a static file server
- Both services are configured with health checks and restart policies
