# IAConsult Architecture Standard

This document defines the architectural principles and structural standards for all IAConsult projects.

---

## 1️⃣ Core Principles

### Security First
- Role-Based Access Control (RBAC)
- Least privilege access
- No hardcoded secrets
- Environment-based configuration

### Multi-Tenant by Design
- Tenant isolation at database level
- agency_id / tenant_id enforced across entities
- Logical separation of client data

### Modular Architecture
- Clear separation between:
  - Frontend (Web / Dashboard)
  - Backend (API)
  - Workers / Background jobs
  - Infrastructure layer

### Scalability
- Stateless API design
- Horizontal scaling ready
- Container-friendly services (Docker-ready)

### Observability
- Structured logging
- Health check endpoints
- Error monitoring ready

---

## 2️⃣ Standard SaaS Structure (Reference)

Typical scalable project layout:

/apps  
/apps/web          → Frontend (Next.js / React)  
/apps/api          → Backend (Node.js / TypeScript)  
/packages/shared   → Shared types & utilities  
/infra             → Docker, Nginx, Traefik, CI/CD  
/docs              → Architecture & documentation  

---

## 3️⃣ Deployment Philosophy

Development → dev branch  
Production → main branch  

- No direct push to main  
- CI must pass before merge  
- Production deploy triggered from main only  

---

## 4️⃣ Infrastructure Guidelines

- VPS-based deployment (Ubuntu LTS)  
- Dockerized services when possible  
- Reverse proxy (Nginx or Traefik)  
- HTTPS enforced (Let's Encrypt)  

---

## 5️⃣ Security Standards

Secrets managed via:
- .env (local only)  
- GitHub Secrets (CI/CD)  
- Server environment variables  

Never commit:
- API keys  
- Private certificates  
- Passwords  

---

## 6️⃣ Future Evolution

All IAConsult SaaS systems must be:
- Multi-tenant ready  
- Cloud scalable  
- Secure by default  
- Automation-driven  

---

Maintained by IAConsult Engineering
