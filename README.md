# ??? Application Security Lab

A personal lab for learning and practicing **Application Security Testing** using vulnerable applications, automated tools, and DevSecOps pipelines.

---

## ?? Purpose
- Document installation and configuration of AppSec tools.
- Practice OWASP Top 10 & API Security vulnerabilities.
- Build a public portfolio of security lab work.
- Learn and demonstrate DevSecOps pipeline integration.

---

## ?? Repository Structure

application-security-lab/
¦
+-- setup/ # Installation & setup docs
¦ +-- tools_checklist.md
¦ +-- tools_installation.md
¦ +-- docker_commands.md
¦
+-- labs/ # Hands-on lab writeups
¦ +-- dvwa/
¦ +-- juice-shop/
¦
+-- payloads/ # Common payloads & cheatsheets
¦
+-- pipelines/ # DevSecOps automation scripts
¦
+-- README.md



---

## ?? Tools Used
- **Core:** Docker, Git, Python 3
- **Security Testing:** Nmap, OWASP ZAP, Burp Suite, Postman
- **Fuzzing & Recon:** ffuf, nuclei, subfinder
- **DevSecOps:** Trivy, OWASP Dependency-Check, Checkov
- **Vulnerable Apps:** DVWA, Juice Shop, crAPI

---

## ?? Getting Started

### 1?? Clone the repository
```bash
git clone https://github.com/kartik3129/application-security-lab.git
cd application-security-lab


2?? Install tools

Follow Tools Installation Guide to set up all required tools.

3?? Verify setup

Use Tools Checklist to confirm everything is installed and working.

4?? Start containers

Use Docker Commands to start and stop vulnerable applications.