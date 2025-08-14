# ?? Docker Commands – AppSec Lab

This document contains common **Docker** commands for starting, stopping, and managing our vulnerable applications and tools in the Application Security Lab.

---

## 1?? Core Docker Commands

```bash
# Check Docker version
docker --version

# List running containers
docker ps

# List all containers (including stopped ones)
docker ps -a

# List downloaded images
docker images

# Stop a running container
docker stop <container_id>

# Remove a container
docker rm <container_id>

# Remove an image
docker rmi <image_id>

# Pull an image from Docker Hub
docker pull <image_name>

# Run a container from an image
docker run <options> <image_name>


2 Vulnerable Applications – Start Commands
DVWA (Damn Vulnerable Web App)

docker pull vulnerables/web-dvwa
docker run --rm -it -p 80:80 vulnerables/web-dvwa

Access: http://localhost

Default Credentials:

username: admin
password: password

OWASP Juice Shop

docker pull bkimminich/juice-shop
docker run --rm -p 3000:3000 bkimminich/juice-shop

Access:http://localhost:3000



crAPI (Completely Ridiculous API)

git clone https://github.com/OWASP/crAPI.git
cd crAPI
docker-compose up -d

Access: As per crAPI documentation (usually port 8888 for web, 5000+ for APIs)

Stop:

docker-compose down


# Stop all running containers
docker stop $(docker ps -q)

# Remove all stopped containers
docker rm $(docker ps -a -q)

# Remove all unused images
docker image prune -a


Tip: Always check docker ps before starting a new container to avoid port conflicts.

