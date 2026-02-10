# ⌚ Ben 10 - Alien Interface

![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
![License](https://img.shields.io/github/license/IshuAgrawal11/ben10?style=for-the-badge)

## 🚀 Project Overview

**Ben 10** is a modern Single Page Application (SPA) built with **React** and **Vite**, designed to demonstrate a complete DevOps workflow. The application serves as a [write a short description: e.g., interactive character dashboard / alien database / mini-game] inspired by the Ben 10 universe.

Beyond the frontend, this project focuses on **containerization and production-grade deployment**. It features a multi-stage Docker build that optimizes the final image size and uses Nginx as a high-performance reverse proxy.

## ✨ Features

### 💻 Frontend
* **Lightning Fast:** Built with Vite for instant server start and HMR.
* **Responsive Design:** optimized for mobile and desktop views.
* **Modern UI:** Developed using React functional components and hooks.

### ⚙️ DevOps & Infrastructure
* **Dockerized:** Fully containerized application for consistent environments.
* **Multi-Stage Build:** optimized Dockerfile reduces image size by ~90% (uses `node:alpine` for building and `nginx:alpine` for serving).
* **Production Ready:** Nginx configured to handle SPA routing and serve static assets efficiently.
* **Orchestration:** Includes `docker-compose.yml` for easy local deployment.

## 🛠️ Tech Stack

* **Frontend Framework:** React 18
* **Build Tool:** Vite
* **Containerization:** Docker
* **Web Server:** Nginx (Alpine Linux)
* **Version Control:** Git & GitHub

## 🐳 Getting Started (Docker)

The easiest way to run this application is using Docker. You do not need Node.js installed on your machine.

### Prerequisites
* Docker
* Docker Compose

## 1. Clone the Repository
```bash
git clone [https://github.com/IshuAgrawal11/ben10.git]
cd ben10
```

## 2. Run with Docker Compose

This will pull the latest image from Docker Hub and start the service.

```bash
docker compose up -d
```

Open your browser and visit:
👉 [http://localhost:8000](http://localhost:8000)

---

## 3. Stop the Application

```bash
docker compose down
```

---

## 🔧 Local Development (Manual)

If you want to edit the code, you can run it locally without Docker.

### Install Dependencies

```bash
npm install
```

### Start Dev Server

```bash
npm run dev
```

### Build for Production

```bash
npm run build
```

---

## 📂 Project Structure

```plaintext
ben10/
├── public/            # Static assets
├── src/               # React source code
├── Dockerfile         # Multi-stage Docker configuration
├── docker-compose.yml # Container orchestration config
├── nginx.conf         # Nginx configuration for SPA routing
├── package.json       # Dependencies and scripts
└── README.md          # Project documentation
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the Project
2. Create your Feature Branch

   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. Commit your Changes

   ```bash
   git commit -m "Add some AmazingFeature"
   ```
4. Push to the Branch

   ```bash
   git push origin feature/AmazingFeature
   ```
5. Open a Pull Request

---

## Architecture Overview

The application follows a clean and production-oriented architecture designed for scalability, performance, and maintainability.

### High-Level Flow

```plaintext
┌────────────┐
│   Browser  │
│ (End User) │
└─────┬──────┘
      │ HTTP Requests
      ▼
┌────────────┐
│   Nginx    │
│ (Alpine)   │
│ Reverse    │
│ Proxy +    │
│ Static     │
│ File Host  │
└─────┬──────┘
      │ Serves Built Assets
      ▼
┌────────────┐
│ React SPA  │
│ (Vite      │
│  Build)    │
└────────────┘
```

### Container Build Strategy

* **Stage 1 – Build**

  * Base Image: `node:alpine`
  * Installs dependencies and generates optimized production assets using Vite

* **Stage 2 – Runtime**

  * Base Image: `nginx:alpine`
  * Serves static files and handles SPA routing
  * Minimal image size and reduced attack surface

This approach ensures fast builds, smaller images, and clean separation between build-time and runtime concerns.

---

## Why This Project?

This project was created to demonstrate **real-world frontend deployment practices**, not just UI development.

Key objectives include:

* Applying **production-grade Docker workflows** to a React application
* Understanding **multi-stage Docker builds** and image optimization
* Configuring **Nginx for Single Page Applications**
* Providing a clean example of **frontend DevOps fundamentals**
* Building a project that reflects **how modern teams ship frontend applications**

Rather than focusing only on features, this repository emphasizes **how software is built, packaged, and deployed** in professional environments.

---

## DevOps & Deployment Highlights

* Deterministic builds using Docker
* Zero-runtime Node.js dependency in production
* Optimized static asset delivery via Nginx
* Environment-agnostic deployment (local, cloud VM, Kubernetes-ready)
* Simple orchestration using Docker Compose

This setup mirrors how frontend services are deployed in many real-world production systems.

---

## Use Cases

This repository can be used as:

* A **DevOps portfolio project**
* A **reference template** for React + Docker deployments
* A **learning resource** for containerized frontend applications
* A starting point for deploying SPAs to cloud platforms (AWS, GCP, Azure)

---

## Future Improvements

Planned or possible enhancements include:

* CI/CD pipeline using GitHub Actions
* Automated Docker image publishing
* Environment-based configuration support
* HTTPS support with reverse proxy (Traefik / Nginx SSL)
* Kubernetes deployment manifests
* Performance and Lighthouse optimizations

---

## Interview Talking Points

If you’re discussing this project in interviews, strong highlights include:

* Why multi-stage Docker builds matter
* How Nginx handles SPA routing (`try_files` strategy)
* Trade-offs between Node-based servers and static hosting
* Benefits of containerized frontend deployments
* Image size optimization and security considerations

---


## 📜 License

Distributed under the **MIT License**.
See `LICENSE` for more information.

---

### 👨‍💻 Created by **Ishu Agrawal**

---


