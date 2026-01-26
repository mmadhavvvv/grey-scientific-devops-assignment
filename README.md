# Grey Scientific Labs – DevOps Assignment 🚀

A comprehensive submission for the DevOps engineering assessment at Grey Scientific Labs, demonstrating containerization strategies and CI/CD pipeline design.

## 🏗️ System Architecture

The project features a decoupled three-tier architecture:
- **Nginx Reverse Proxy**: Entry point handling routing and load balancing.
- **Frontend**: Serves static content via Nginx.
- **Backend**: Application logic layer communicating with the database.
- **PostgreSQL Database**: Persistent storage layer.

**Traffic Flow:**
`User → Nginx (Load Balancer) → Frontend/Backend → PostgreSQL`

## 🛠️ Infrastructure & DevOps

### 🐳 Dockerized Environment
The entire stack is orchestrated using **Docker Compose**, featuring:
- **Isolated Networks**: Secure communication between services.
- **Persistent Volumes**: Ensuring data durability for PostgreSQL.
- **Restart Policies**: Automatic recovery for high availability.

### ⛓️ CI/CD Pipeline
Includes a **Jenkins** pipeline definition (`Jenkinsfile`) with the following stages:
1.  **Source**: Code ingestion from GitHub.
2.  **Build**: Generation of optimized Docker images.
3.  **Test**: Placeholder for automated unit and integration tests.
4.  **Deploy**: Automated deployment using Docker Compose.

## 📁 Repository Structure

- `cicd/`: Pipeline definitions and automation scripts.
- `nginx/`: Proxy configuration and frontend assets.
- `docker-compose.yml`: Main orchestration file.

## 🚀 Deployment

To spin up the entire environment locally:

```bash
docker-compose up -d
```

The system will be accessible via Nginx on the configured host port.

---
*Developed by Madhav Khanna for Grey Scientific Labs.*
