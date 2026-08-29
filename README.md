## 3️⃣ README for `MERN-Production`

# MERN Backend — Production

A robust, enterprise-grade backend application built with **Express.js** and **TypeScript**, designed for production deployment. This backend provides comprehensive APIs for a SaaS/blog platform with advanced features including AI integration, email services, and cloud storage.

## 📋 Overview
Production-ready Node.js backend for a MERN (MongoDB, Express, React, Node.js) stack application. It features enterprise-level security, scalability, and monitoring capabilities, with a fully containerized deployment pipeline.

## 🛠 Tech Stack
- **Runtime:** Node.js, Express.js (v5), TypeScript
- **Database:** MongoDB (Mongoose)
- **Auth:** JWT, Bcrypt
- **Email:** Nodemailer, SendGrid
- **AI:** Voyoga AI
- **Monitoring:** Prometheus (prom-client), Morgan logging
- **Containerization:** Docker

## ✨ Features
- JWT-based authentication with bcrypt password hashing
- RESTful APIs with standardized success/error responses
- Email services (Nodemailer + SendGrid)
- AI-powered features (Voyoga AI)
- Prometheus metrics at `/metrics` and health check at `/health`
- CORS configuration and environment-based config management

## ☁️ Deployment (AWS)
The application is deployed on **AWS**:
- Backend hosted on AWS cloud infrastructure
- Dockerized for consistent deployment
- **Cloudflare** for DNS, security, and traffic management
- Custom domain with **HTTPS / SSL**
- CI/CD pipeline with GitHub Actions and Jenkins for automated builds & deployments

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or later)
- npm
- MongoDB instance (local or Atlas)
- Docker (optional, for containerized deployment)

### Installation
```bash
git clone https://github.com/namal1230/MERN-BE-Production.git
cd MERN-BE-Production
npm install
```
# Environment Setup
Create a .env file in the root directory:<br>
PORT=5000<br>
NODE_ENV=development<br>
MONGODB_URI=<your_mongodb_connection_string><br>
JWT_SECRET=<your_jwt_secret><br>
CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name><br>
CLOUDINARY_API_KEY=<your_cloudinary_api_key><br>
CLOUDINARY_API_SECRET=<your_cloudinary_api_secret><br>
SENDGRID_API_KEY=<your_sendgrid_api_key><br>
OPENAI_API_KEY=<your_openai_api_key><br>

# Development
npm run dev<br>
Production Build<br>
npm run build<br>
npm start<br>

## Docker
docker build -t mern-backend .<br>
docker run -p 5000:5000 --env-file .env mern-backend<br>

# 📡 API Documentation
Base URL: http://localhost:5000<br>
Success Response:<br>
{ "success": true, "data": {}, "message": "Operation successful" }<br>
Error Response:<br>
{ "success": false, "error": "Error message", "statusCode": 400 }<br>
Authentication: Include JWT token in request headers:<br>
Authorization: Bearer <your_jwt_token><br>

# Key Endpoints:
- GET /health — health check<br>
- GET /metrics — Prometheus metrics<br>
- Refer to route files in src/routes/ for complete API documentation<br>

# 📁 Project Structure

├── src/<br>
│   ├── routes/<br>
│   ├── controllers/<br>
│   ├── models/<br>
│   ├── middleware/<br>
│   └── config/<br>
├── Dockerfile<br>
├── Jenkinsfile<br>
├── compose.yaml<br>
├── terraform/<br>
└── prometheus.yml<br>

# 🔒 Security

✅ JWT-based authentication, bcrypt password hashing, CORS configuration, environment variable management, input validation via Mongoose schemas.

# 🤝 Contributing

1. Fork the repository
2. Create a feature branch: git checkout -b feature/your-feature
3. Commit changes: git commit -m 'Add feature'
4. Push and open a Pull Request
   
# 📄 License
ISC License — see package.json for details.
Author: namal1230 (https://github.com/namal1230)
