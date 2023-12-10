# Kira CORS Anywhere

### Overview

Kira CORS Anywhere is a project designed to set up a CORS Anywhere server with SSL from Let's Encrypt. It leverages GitHub Actions for deployment and Ansible for server configuration and management.

### Features

* Automated deployment on pull requests and specific branches.
* Secure SSL configuration using Let's Encrypt.
* Easy setup and configuration with Ansible and Terraform.

### Prerequisites
A Hetzner Cloud account.
GitHub account for deploying the workflow.
Ansible and Terraform installed for local setup and testing.
GitHub Workflow: Hetzner Deploy on PR
This GitHub Action workflow is triggered on pull requests to the master branch and pushes to feature/* and bugfix/* branches. It includes steps for setting up Python, Ansible, and Terraform, and concludes with deploying the configuration on Hetzner Cloud.

### Key Steps:

1. Checking out the repository.
2. Setting up Python and Ansible.
3. Initializing and applying Terraform configuration.
4. Retrieving the IP address of the VM.
5. Running the Ansible playbook cors-anywhere-playbook.yml.

### Environment Variables and Secrets:

HCLOUD_TOKEN: Authentication token for Hetzner Cloud.
ANSIBLE_SSH_PRIVATE_KEY: SSH private key for Ansible.
Ansible Playbook: Set up CORS Anywhere Server with SSL
The Ansible playbook cors-anywhere-playbook.yml is used for setting up the CORS Anywhere server with SSL from Let's Encrypt on a specified server.

### Key Tasks:

1. Updating and upgrading apt packages.
2. Installing Node.js, NPM, nginx, and necessary packages.
3. Adding the Certbot repository and installing Certbot.
4. Obtaining an SSL certificate from Let's Encrypt.
5. Cloning the CORS Anywhere repository and installing dependencies.
6. Creating and enabling the Nginx configuration for CORS Anywhere.
7. Starting the CORS Anywhere server.
8. Installation

### Usage
[TODO]

### Contributing
[TODO]

### License
[TODO]
