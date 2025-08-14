# 🛡️ Application Security Lab – Tools Checklist ✅

## 1. Core Setup
- [ ] **Docker Desktop** – Installed & running  
  - Check: `docker --version`  
  - Check: `docker ps` (should not give an error)
- [ ] **Git** – Installed & configured  
  - Check: `git --version`
- [ ] **Python 3 + pip** – Installed  
  - Check: `python --version`  
  - Check: `pip --version`

---

## 2. Security Tools
- [ ] **Nmap** – Network scanner  
  - Check: `nmap --version`
- [ ] **OWASP ZAP** – DAST tool  
  - Check: Launch GUI or run `zap.sh -h`
- [ ] **Burp Suite (Community Edition)** – Web proxy/scanner  
  - Check: Launch GUI
- [ ] **Postman** – API testing  
  - Check: Launch and send a test request
- [ ] **ffuf** – Fuzzing URLs/parameters  
  - Check: `ffuf -h`
- [ ] **nuclei** – Vulnerability scanning templates  
  - Check: `nuclei -version`
- [ ] **subfinder** – Subdomain enumeration  
  - Check: `subfinder -version`
- [ ] **Trivy** – Container vulnerability scanning  
  - Check: `trivy -v`
- [ ] **OWASP Dependency-Check** – SCA tool  
  - Check: `dependency-check.sh --version` (or Windows: `.bat`)
- [ ] **Checkov** – IaC scanning  
  - Check: `checkov --version`

---

## 3. Vulnerable Applications (Docker)
- [ ] **DVWA** – Damn Vulnerable Web App  
  - Pull: `docker pull vulnerables/web-dvwa`  
  - Run: `docker run --rm -it -p 80:80 vulnerables/web-dvwa`  
  - Access: [http://localhost](http://localhost)
- [ ] **OWASP Juice Shop** – Modern web vulnerabilities  
  - Pull: `docker pull bkimminich/juice-shop`  
  - Run: `docker run --rm -p 3000:3000 bkimminich/juice-shop`  
  - Access: [http://localhost:3000](http://localhost:3000)
- [ ] **crAPI** – API security testing  
  - Repo: [https://github.com/OWASP/crAPI](https://github.com/OWASP/crAPI)  
  - Setup: `docker-compose up -d` (from project folder)  
  - Access: As per crAPI docs

---

## 4. Verification Commands
```bash
docker ps         # Check running containers
docker images     # Check available images
zap.sh -version   # Check ZAP version
burpsuite         # Launch Burp (if added to PATH)
