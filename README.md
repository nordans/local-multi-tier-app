# 🧱 Automated Local Multi-Tier Web Application

This project sets up a **local multi-tier web application environment** using **Vagrant and Bash provisioning scripts**.  
It simulates a production-like architecture with components like NGINX, Tomcat, MySQL, Memcached, and RabbitMQ — all running on a single Ubuntu virtual machine.

---

## 🧪 Architecture

[Client]
↓
[NGINX]
↓
[Java App on Tomcat]
  ↙︎       ↘︎
[MySQL] [Memcached]
↓
[RabbitMQ]


---

## ⚙️ Technology Stack

| Layer         | Technology          |
|---------------|---------------------|
| Provisioning  | Vagrant + Bash      |
| Backend       | Java (Spring Boot)  |
| App Server    | Apache Tomcat       |
| Reverse Proxy | NGINX               |
| Database      | MySQL               |
| Cache         | Memcached           |
| Message Queue | RabbitMQ            |

---

## 📁 Project Structure

local-multi-tier-app/
├── AutomatedLocalApp/
│ ├── Vagrantfile
│ ├── application.properties
│ ├── backend.sh
│ ├── mysql.sh
│ ├── memcache.sh
│ ├── rabbitmq.sh
│ ├── nginx.sh
│ ├── tomcat.sh
│ └── tomcat_ubuntu.sh
├── pom.xml
├── src/
└── README.md


---

## 🚀 Getting Started

### Prerequisites

- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)

### Launch the Environment

```bash
cd AutomatedLocalApp
vagrant up

    This will automatically provision an Ubuntu VM with all required services.

🌐 Access Points
Service	URL/Port
NGINX	http://localhost:8080
Backend API	http://localhost:8080/api/...
MySQL	localhost:3306
RabbitMQ	localhost:5672
Memcached	localhost:11211
🧪 Testing

    Access the app using a browser or Postman.

    Check services via SSH:

vagrant ssh
sudo systemctl status nginx

📌 Notes

    This setup emulates a real-world on-premise deployment.

    Easily extendable to Docker, Kubernetes, or cloud environments like AWS.

    Great foundation for integrating CI/CD tools (e.g., Jenkins, GitHub Actions, Ansible).

👨‍💻 Author

Norman Świątek

    GitHub: @nordans

    Portfolio: https://normandev.xyz

