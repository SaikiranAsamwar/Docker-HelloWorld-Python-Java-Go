# Docker Setup and Hello World Projects

This repository documents the installation of Docker and building/running simple Hello World applications in **Python**, **Java**, and **Go** using Docker.

---

## 🚀 Docker Installation & Setup

```bash
# Update packages
sudo yum update -y

# Install Docker
sudo yum install docker -y

# Check Docker version
docker --version

# Start and enable Docker service
sudo systemctl start docker
sudo systemctl enable docker

# Install Docker Compose (v2.27.0)
sudo mkdir -p /usr/local/lib/docker/cli-plugins
sudo curl -SL https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64 \
     -o /usr/local/lib/docker/cli-plugins/docker-compose
sudo chmod +x /usr/local/lib/docker/cli-plugins/docker-compose

# Verify installation
docker compose version
```

---

## 🔧 Git Installation & Configuration

```bash
# Install Git
sudo yum install git -y

# Configure Git user
git config --global user.name "Saikiran Asamwar"
git config --global user.email "saikiranasamwar@gmail.com"

# Verify Git configuration
git config --list
```

---

## 🐍 Python Hello World

```bash
# Clone repository
git clone https://github.com/atulkamble/pythonhelloworld.git
cd pythonhelloworld/

# Install Python (for local testing)
sudo yum install python3 -y
python3 helloworld.py   # Run locally (optional)

# Build Docker image
sudo docker build -t saikiranasamwar4/pythonhelloworld .

# Push image to Docker Hub
sudo docker push saikiranasamwar4/pythonhelloworld

# Run container
sudo docker run -d -p 80:80 saikiranasamwar4/pythonhelloworld
```

---

## ☕ Java Hello World

```bash
# Clone repository
git clone https://github.com/atulkamble/javahelloworld.git
cd javahelloworld/

# Install Java (for local testing)
sudo yum install java -y
java helloworld   # Run locally (optional)

# Build Docker image
sudo docker build -t saikiranasamwar4/javahelloworld .

# Push to Docker Hub
sudo docker push saikiranasamwar4/javahelloworld

# Run container
sudo docker run -d -p 8080:8080 saikiranasamwar4/javahelloworld
```

---

## 🐹 Go Hello World

```bash
# Clone repository
git clone https://github.com/atulkamble/gohelloworld.git
cd gohelloworld/

# Install Go (for local testing)
sudo yum install go -y
go run helloworld.go   # Run locally (optional)

# Build Docker image
sudo docker build -t saikiranasamwar4/gohelloworld .

# Push to Docker Hub
sudo docker push saikiranasamwar4/gohelloworld

# Run container
sudo docker run -d -p 9090:9090 saikiranasamwar4/gohelloworld
```

---

## 🛠 Useful Docker Commands

```bash
# List images
sudo docker images

# List running containers
sudo docker container ls

# List all containers (running + stopped)
sudo docker container ps -a

# Remove image
sudo docker rmi <image_name>
```

---

## 👨‍💻 Author

**Saikiran Rajesh Asamwar**  
- Full Stack MERN Developer | Certified AWS Cloud Engineer | Aspiring DevOps Engineer  
- GitHub: [SaikiranAsamwar](https://github.com/SaikiranAsamwar)  
- Email: saikiranasamwar@gmail.com  

---

✅ With these steps, you can run **Hello World apps in Python, Java, and Go** inside Docker containers and push them to Docker Hub.  
