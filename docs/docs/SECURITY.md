# IAConsult Security Standards

This document defines the mandatory security practices for all IAConsult projects.

---

## 1️⃣ Secret Management

Never commit:

- API keys
- Private SSH keys
- Database credentials
- JWT secrets
- SSL certificates
- .env files

Use instead:

- .env (local development only)
- GitHub Secrets (CI/CD)
- Server environment variables (production)

---

## 2️⃣ Access Control

All systems must implement:

- Role-Based Access Control (RBAC)
- Least privilege principle
- Separation between admin and user roles
- Audit logging for sensitive actions

---

## 3️⃣ VPS Security Guidelines

Production servers must follow:

- Ubuntu LTS only
- Firewall enabled (UFW)
- SSH key authentication preferred
- Root login disabled when possible
- Fail2Ban recommended
- Automatic security updates enabled

---

## 4️⃣ Repository Protection

All production repositories must:

- Protect main branch
- Require pull request before merge
- Require CI checks to pass
- Disallow force push to main

---

## 5️⃣ Data Protection

- Tenant isolation enforced
- Sensitive data encrypted when possible
- HTTPS mandatory
- Backup strategy defined
- Regular security review

---

## 6️⃣ Incident Response

In case of security incident:

1. Revoke compromised credentials
2. Rotate secrets immediately
3. Audit logs
4. Patch vulnerability
5. Document incident

---

Security is not optional.  
It is part of IAConsult engineering DNA.

Maintained by IAConsult Engineering
