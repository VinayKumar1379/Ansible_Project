🚀 Ansible Project – Automation & Configuration Management

This repository contains Ansible playbooks and configurations used to automate server setup, configuration management, and deployment tasks in a Linux/cloud environment.

📌 Project Overview

This project demonstrates how to use Ansible for:

Automating server provisioning
Managing configurations across multiple servers
Performing application deployments
Executing remote administrative tasks

It follows a cloud-native approach and leverages automation to reduce manual effort and ensure consistency.

🛠️ Tech Stack
Ansible
Linux (RHEL / Ubuntu)
SSH
Cloud Platforms (AWS / Azure / GCP)
YAML
📂 Project Structure
Ansible_Project/
│── inventory/           # Inventory files (hosts)
│── playbooks/           # Main Ansible playbooks
│── roles/               # Reusable roles (if used)
│── group_vars/          # Group variables
│── host_vars/           # Host-specific variables
│── ansible.cfg          # Ansible configuration file
⚙️ Prerequisites

Make sure you have the following installed:

Ansible (v2.9+ recommended)
Python (3.x)
SSH access to target servers
Proper inventory configuration

Install Ansible:

sudo yum install ansible -y     # RHEL/CentOS
sudo apt install ansible -y     # Ubuntu/Debian
🔑 Setup & Configuration
Clone the repository:
git clone https://github.com/VinayKumar1379/Ansible_Project.git
cd Ansible_Project
Update inventory file:
nano inventory/hosts
Add your target servers:
[web]
192.168.1.10

[db]
192.168.1.20
Test connectivity:
ansible all -m ping
▶️ Usage

Run a playbook:

ansible-playbook -i inventory/hosts playbooks/main.yml

Run with specific group:

ansible-playbook -i inventory/hosts playbooks/main.yml -l web
