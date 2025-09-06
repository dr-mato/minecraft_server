# Minecraft Server Infrastructure

This repository documents the infrastructure, automation, and workflows built to provision, manage, and maintain a fully functional Minecraft multiplayer server.  

Originally created as a learning playground, the project evolved into a **complete DevOps exercise**, integrating modern infrastructure practices such as Infrastructure-as-Code, containerization, CI/CD pipelines, and automated documentation.

---

## Highlights

- **Cloud Hosting**  
  - Deployed on **DigitalOcean**, provisioned automatically  
  - Configured with **cloud-init** during server boot  

- **Infrastructure as Code**  
  - **Ansible** playbooks for provisioning, deployment, and teardown  
  - Secrets managed via **GitHub repository settings** and Ansible variables  

- **Containerization**  
  - Minecraft server packaged as a **Docker image** for reproducibility  
  - CI workflow to build and publish images  

- **Automation & Workflows**  
  - **GitHub Actions pipelines** for:  
    - `backup` – regular server/world data backups  
    - `create_do_server` – spin up new DigitalOcean instances  
    - `create_mc_alias` – DNS/alias management  
    - `create_minecraft_docker_image` – image build pipeline  
    - `update_wiki` – auto-publish documentation  

- **Documentation & Collaboration**  
  - Internal wiki auto-updated from pipelines  
  - Pre-commit hooks for code consistency  
  - GitHub Projects used for ticket tracking  

---

## Skills Demonstrated

- **Infrastructure Automation**: Provisioning and configuration with Ansible + cloud-init  
- **Cloud Services**: Hands-on with DigitalOcean droplets, networking, and DNS  
- **CI/CD**: GitHub Actions for backups, image builds, deployment, and documentation updates  
- **Containerization**: Docker-based deployment for portability and reproducibility  
- **Collaboration**: Wiki-driven documentation, pre-commit hooks, GitHub Projects for agile task tracking  

---

## Getting Started

> This project was tailored for private use but can be adapted by others.  

### Prerequisites
- DigitalOcean API token  
- Ansible installed locally  
- Docker installed locally  

### Deployment
```bash
git clone https://github.com/ntatrishvili/minecraft_server.git
cd minecraft_server
ansible-playbook create_server.yml
ansible-playbook deploy_minecraft.yml
```
Backups and updates are managed by GitHub Actions workflows.

## Lessons Learned

This project started as a game server and became a practical lab for modern DevOps practices.  
Key takeaways included:  
- Automating full server lifecycles with Infrastructure-as-Code  
- Reliable backup/recovery using pipelines  
- Reproducible deployments with Docker  
- Team collaboration workflows with GitHub Projects and automated documentation  

---

## Status

This repository is archived as an **educational DevOps experiment**.  
The concepts and patterns are applicable to production-grade infrastructure projects.  

