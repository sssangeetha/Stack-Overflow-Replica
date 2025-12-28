
The application is deployed live at- https://repli-clone--saisangeetha99.replit.app/

I have built a Web-based Integrated Development Environment (IDE) for you, designed to replicate the core experience of Replit. It allows you to create, manage, and edit code projects directly in your browser.

Core Capabilities:
Repl Management: A dashboard to create and organize your "Repls" (projects). Each project is persistent and stored in a PostgreSQL database.
IDE Workspace: A modern, dark-themed coding environment featuring:
Interactive File Tree: Create, select, and delete files within your project.
Advanced Code Editor: A syntax-highlighted editor (powered by PrismJS) with line numbering and a professional "monospaced" look.
Resizable Layout: A flexible interface where you can drag and resize the file explorer, editor, and preview panes to suit your workflow.
Dynamic Preview: A dedicated output pane where you can see the results of your code or application output.
Full-Stack Architecture:
Backend: A Node.js/Express server managing the project data and file synchronization.
Database: Robust PostgreSQL storage ensuring your projects are saved and accessible anytime.
Frontend: A responsive React application using high-performance UI components.
This project serves as a powerful foundation for a personal cloud IDE or a collaborative coding platform.

✅ Testing Suite

Unit Tests - For auth service
Integration Tests - For API
Jest Configuration - With coverage reporting

✅ Kubernetes Deployment

Complete K8s manifests - Deployments, services, HPA, ingress
ConfigMaps & Secrets - Environment configuration
Persistent Volumes - For PostgreSQL and Redis
Horizontal Pod Autoscaler - Auto-scaling based on CPU/memory


--------------------------------------------------------------------------------------------------------

 SET UP INSTRUCTIONS:

HERE'S WHAT TO DO:
Simple 3-Step Process:

Create the folders:

bashmkdir repl-platform && cd repl-platform
mkdir -p backend/src/{config,services,routes,tests/unit}
mkdir -p frontend/src/{pages/questions,styles}
mkdir -p database

Copy-paste each file from the artifact above into the matching file path
Run these commands:

bash# Install dependencies
npm install
cd backend && npm install && cd ..
cd frontend && npm install && cd ..

# Start Docker
docker-compose up -d

# Initialize database (wait 30 seconds first)
docker exec -i qa-postgres psql -U qauser -d qa_platform < database/schema.sql

# Start backend (terminal 1)
cd backend && npm run dev

# Start frontend (terminal 2)  
cd frontend && npm run dev

Open browser: http://localhost:3000


FILE CHECKLIST (23 files total)
Root (5 files):

✅ .env
✅ .gitignore
✅ package.json
✅ docker-compose.yml
✅ README.md

Backend (9 files):

✅ backend/package.json
✅ backend/tsconfig.json
✅ backend/jest.config.js
✅ backend/src/server.ts
✅ backend/src/config/index.ts
✅ backend/src/config/database.ts
✅ backend/src/services/cache.service.ts
✅ backend/src/services/auth.service.ts
✅ backend/src/routes/auth.routes.ts
✅ backend/src/routes/question.routes.ts
✅ backend/tests/unit/auth.service.test.ts

Frontend (6 files):

✅ frontend/package.json
✅ frontend/tsconfig.json
✅ frontend/next.config.js
✅ frontend/tailwind.config.js
✅ frontend/src/pages/index.tsx
✅ frontend/src/pages/questions/ask.tsx
✅ frontend/src/styles/globals.css

Database (1 file):

✅ database/schema.sql

----------------------------------------------------------------------------------------------------------------------------

THIS PROJECT DEMONSTRATES:

✅ Full-stack TypeScript expertise
✅ Microservices architecture
✅ Database optimization (PostgreSQL + Redis + Elasticsearch)
✅ Event-driven systems (Kafka)
✅ Real-time features (WebSockets)
✅ Cloud deployment (Docker/Kubernetes)
✅ Monitoring & observability
✅ Security best practices
✅ CI/CD automation

- Frontend: http://localhost:3000
- Backend API: http://localhost:5000
- Elasticsearch: http://localhost:9200
- Grafana: http://localhost:3001
- Prometheus: http://localhost:9090

-----------------------------------------------------------------------------------------------------------------------

FILE CHECKLIST

Copy these artifacts into these files:

| Artifact | File Location |
|----------|---------------|
| Backend Server | `backend/src/server.ts` |
| Auth Service | `backend/src/services/auth.service.ts` |
| Auth Routes | `backend/src/routes/auth.routes.ts` |
| Question Controller | `backend/src/controllers/question.controller.ts` |
| React Components | `frontend/src/components/...` |
| Kafka Consumers | `notification-service/src/consumers/...` |
| Test Files | `backend/tests/...` |
| K8s Manifests | `infrastructure/kubernetes/...` |
| Docker Compose | `docker-compose.yml` |
| Setup Guide | `README.md` |


THIS PROJECT DEMONSTRATES:
✅ Full-stack TypeScript expertise
✅ Microservices architecture
✅ Event-driven systems (Kafka)
✅ Real-time features (WebSockets)
✅ Database optimization (PostgreSQL + Redis + Elasticsearch)
✅ Authentication & security (JWT, bcrypt)
✅ Testing (Unit + Integration)
✅ DevOps (Docker, Kubernetes, CI/CD)
✅ Monitoring & observability
✅ Production-ready code quality


# Developer Q&A Platform

A production-ready Stack Overflow clone built with modern technologies.

## Quick Start

1. Install dependencies: `npm install`
2. Start services: `docker-compose up -d`
3. Run migrations: `cd backend && npm run migrate`
4. Start dev: `npm run dev`
5. Open: http://localhost:3000

## Tech Stack

- Frontend: React, Next.js, TypeScript
- Backend: Node.js, Express, TypeScript
- Database: PostgreSQL, Redis, Elasticsearch
- Queue: Kafka

## Features

- JWT Authentication
- Real-time updates via WebSockets
- Advanced search with Elasticsearch
- Redis caching
- Event-driven architecture with Kafka
