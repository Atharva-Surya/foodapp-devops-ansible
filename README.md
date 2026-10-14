# FoodApp DevOps Case Study & Ansible Automation

## Overview
This project demonstrates configuration management and automated web server deployment for a sample online food-ordering application called FoodApp.

## Technologies Used
- Ansible
- Nginx
- Ubuntu Linux (WSL2)
- YAML
- Jinja2 templates

## Project Structure
```text
.
├── inventory.ini
├── site.yml
└── templates/
    ├── nginx.conf.j2
    └── index.html.j2
```

## Implementation
The Ansible playbook automates:
- Installing Nginx
- Creating the application web directory
- Deploying the HTML application page
- Configuring the Nginx server on port 8080
- Managing the Nginx service
- Verifying the application response

## Execution
Check the playbook syntax:

```bash
ansible-playbook -i inventory.ini site.yml --syntax-check
```

Execute the playbook:

```bash
ansible-playbook -i inventory.ini site.yml -K
```

Verify the application:

```bash
curl http://localhost:8080
```

Open `http://localhost:8080` in a browser to view the deployed page.

## Key Concepts
- Infrastructure as Code
- Configuration management
- Idempotency
- Jinja2 templates
- Ansible handlers and tags

## Limitations
The demonstration uses a local Ubuntu WSL2 environment and a static HTML page. CI/CD integration and monitoring are proposed future enhancements.
