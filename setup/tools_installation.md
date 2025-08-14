#  Tools Installation – Application Security Lab

This guide covers installation steps for all core and optional tools in the lab.

---

## 1 Core Setup

### Install Docker Desktop
- **Windows/Mac:** [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
- **Linux (Ubuntu example):**
```bash
sudo apt update
sudo apt install docker.io docker-compose -y
sudo systemctl enable docker
sudo systemctl start docker


Verify:

docker --version
docker-compose --version

Install Git

Windows/Mac: https://git-scm.com/downloads

Linux:

sudo apt install git -y


Verify:

git --version

Install Python 3 + pip

Windows/Mac: https://www.python.org/downloads/

Linux:

sudo apt install python3 python3-pip -y


Verify:

python --version
pip --version

2 Security Tools
Nmap
sudo apt install nmap -y


Verify: nmap --version

OWASP ZAP

Download: https://www.zaproxy.org/download/

Linux (APT):

sudo snap install zaproxy --classic


Verify: Launch GUI or run zap.sh -h

Burp Suite (Community Edition)

Download: https://portswigger.net/burp/communitydownload
Verify: Launch GUI

Postman

Download: https://www.postman.com/downloads/
Verify: Launch and send a test request

ffuf
go install github.com/ffuf/ffuf/v2@latest


(Ensure Go is installed: https://go.dev/dl/)
Verify: ffuf -h

nuclei
go install github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest


Verify: nuclei -version

subfinder
go install github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest


Verify: subfinder -version

Trivy
sudo apt install trivy -y


Verify: trivy -v

OWASP Dependency-Check

Download: https://jeremylong.github.io/DependencyCheck/dependency-check-cli/

Verify: dependency-check.sh --version (Linux/Mac) or .bat (Windows)

Checkov
pip install checkov


Verify: checkov --version

3 Vulnerable Applications (Docker)
DVWA
docker pull vulnerables/web-dvwa
docker run --rm -it -p 80:80 vulnerables/web-dvwa


Access: http://localhost
Default creds: admin / password

OWASP Juice Shop
docker pull bkimminich/juice-shop
docker run --rm -p 3000:3000 bkimminich/juice-shop


Access: http://localhost:3000

crAPI
git clone https://github.com/OWASP/crAPI.git
cd crAPI
docker-compose up -d


Access: As per crAPI documentation

Tip: Install tools in the above order to avoid dependency issues.