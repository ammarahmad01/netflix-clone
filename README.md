# Netflix Clone - DevSecOps Project

A full DevSecOps pipeline deploying a Netflix Clone application on AWS using 
EC2, Docker, Jenkins, SonarQube, Trivy, Prometheus, Grafana, and Kubernetes (EKS).

## Demo Video
https://drive.google.com/file/d/1uggmx_9TrYVdPmyQV0H54rmDYDXG0FSi/view

## Project Phases

### Phase 1 - AWS EC2 Setup
- Launched t2.large EC2 instance (Ubuntu) with Elastic IP
- Configured Security Groups with required ports

### Phase 2 - Security Setup
- Installed Docker and containerized the application
- Integrated TMDB API Key for live movie data

### Phase 3 - CI/CD Pipeline (Jenkins)
- Installed Jenkins with OpenJDK 17
- Configured plugins: SonarQube Scanner, Docker, NodeJS, OWASP Dependency-Check
- Built full Jenkins pipeline with stages:
  - Code Checkout → SonarQube Analysis → Quality Gate
  - OWASP FS Scan → Trivy FS Scan
  - Docker Build & Push → Trivy Image Scan → Deploy

### Phase 4 - Monitoring
- Installed Prometheus + Grafana on separate EC2 instance
- Set up Node Exporter for system metrics
- Created Grafana dashboards for Jenkins performance monitoring

### Phase 6 - Kubernetes (EKS)
- Created AWS EKS cluster with c6a.large node groups
- Installed Helm and Prometheus Node Exporter
- Deployed app using ArgoCD with GitOps workflow
- Configured Load Balancer for external access

## Tech Stack
AWS EC2 | Docker | Jenkins | SonarQube | Trivy | OWASP | 
Prometheus | Grafana | Kubernetes (EKS) | ArgoCD | Helm | Nginx

## Docker Hub
https://hub.docker.com/r/ammar0990/netflix

## Screenshot
<img width="1920" height="977" alt="image" src="https://github.com/user-attachments/assets/284b899f-d233-4618-8218-197c01cd7efc" />
