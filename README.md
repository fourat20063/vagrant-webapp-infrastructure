# Multi-Tier Web Application Stack Automation

## 📖 Overview
This project demonstrates the setup and automation of a **multi-tier web application stack** on a local desktop environment using **Oracle VM VirtualBox** as the hypervisor and **Vagrant** for infrastructure automation.

The infrastructure is composed of **five virtual machines**, each serving a dedicated role in a classic multi-tier architecture. All provisioning is fully automated using shell scripts executed by Vagrant.

This project aims to simulate a real-world production-like environment while running locally.

---

## 🏗 Architecture

User → Load Balancer (NGINX) → Application Server (Tomcat)  
                                     ↙       ↓       ↘  
                             MySQL   Memcached   RabbitMQ  

---

## 🖥️ Technology Stack

### Virtualization & Automation
- **Oracle VM VirtualBox** – Hypervisor
- **Vagrant** – VM lifecycle & provisioning automation
- **Git Bash (CLI)** – Command-line interface

### Operating Systems
- **CentOS** – Load Balancer
- **Ubuntu** – Application & backend services

---

## 🧱 Server Roles

| Server | OS | Role |
|------|----|------|
| Load Balancer | CentOS | NGINX |
| Application Server | Ubuntu | Apache Tomcat |
| Message Broker | Ubuntu | RabbitMQ |
| Caching Layer | Ubuntu | Memcached |
| Database Server | Ubuntu | MySQL |

---

## ⚙️ Provisioning & Automation

- All servers are provisioned automatically using **Vagrant shell provisioners**
- Installation, configuration, and service startup are handled via scripts
- No manual configuration is required after running `vagrant up`

---



