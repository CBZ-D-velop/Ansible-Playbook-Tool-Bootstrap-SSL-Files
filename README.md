# Ansible playbook: tool.bootstrap_ssl_files

![Licence Status](https://img.shields.io/badge/licence-MIT-brightgreen)
![CI Status](https://img.shields.io/badge/CI-success-brightgreen)
![Testing Method](https://img.shields.io/badge/Testing%20Method-Ansible%20Molecule-blueviolet)
![Testing Driver](https://img.shields.io/badge/Testing%20Driver-docker-blueviolet)
![Language Status](https://img.shields.io/badge/language-Ansible-red)
![Compagny](https://img.shields.io/badge/Compagny-Labo--CBZ-blue)
![Author](https://img.shields.io/badge/Author-Lord%20Robin%20Cbz-blue)

## Description

![Tag: Ansible](https://img.shields.io/badge/Tech-Ansible-orange)
![Tag: Debian](https://img.shields.io/badge/Tech-Debian-orange)
![Tag: OpenSSL](https://img.shields.io/badge/Tech-OpenSSL-orange)
![Tag: SSL/TLS](https://img.shields.io/badge/Tech-SSL%2FTLS-orange)
![Tag: KEY](https://img.shields.io/badge/Tech-KEY-orange)
![Tag: REQ](https://img.shields.io/badge/Tech-REQ-orange)
![Tag: CSR](https://img.shields.io/badge/Tech-CSR-orange)
![Tag: CRT](https://img.shields.io/badge/Tech-CRT-orange)
![Tag: PEM](https://img.shields.io/badge/Tech-PEM-orange)
![Tag: CA](https://img.shields.io/badge/Tech-CA-orange)

An Ansible playbook create a list of defined files related to SSL/TLS

The Certificate Management playbook automates the creation and organization of certificates, including Certificate Authorities (CAs), root CAs, intermediate CAs, and end certificates. This playbook simplifies the process of generating certificates and provides a streamlined approach for managing SSL/TLS infrastructure. Key features of this playbook include:

Certificate Creation: The playbook generates various types of certificates, including root CAs, intermediate CAs, and end certificates. It allows you to define the desired SSL/TLS information, such as Common Name (CN), Country (C), State (ST), Locality (L), Organization (O), Organizational Unit (OU), and email address.

Certificate Filing: The playbook organizes the generated certificates into separate components and creates a ZIP archive for each component. This makes it easy to deploy and distribute the certificates to the desired target systems.

Customization Options: The playbook provides flexibility by allowing you to specify the validity period, key size, and base path for storing the certificate files. You can customize these parameters to meet your specific requirements.

By utilizing the Certificate Management playbook, you can simplify the creation and management of SSL/TLS certificates, ensure proper organization and filing of certificates, and streamline the deployment process.

## Deployment diagramm

## Tests and simulations

### Basics

You have to run multiples tests. *tests with an # are mandatory*

```MARKDOWN
# syntax
# converge
# idempotence
# verify
side_effect
```

Executing theses test in this order is called a "scenario" and Molecule can handle them.

Molecule use Ansible and pre configured playbook to create containers, prepare them, converge (run the playbook) and verify its execution.
You can manage multiples scenario with multiples tests in order to get a 100% code coverage.

This playbook contains a ./tests folder. In this folder you can use the inventory or the tower folder to create a simualtion of a real inventory and a real AWX / Tower job execution.

### Command reminder

```SHELL
# Check your YAML syntax
yamllint -c ./.yamllint .

# Check your Ansible syntax and code security
ansible-lint --config=./.ansible-lint .

# Execute and test your playbook
molecule create
molecule list
molecule converge
molecule verify
molecule destroy

# Execute all previous task in one single command
molecule test
```

## Installation

To install this playbook, just copy/import this playbook or raw file into your fresh playbook repository or call it with the "include_playbook/import_playbook" module.

## Usage

### Vars

```YAML
# From inventory
---

```

```YAML
# From AWX / Tower
---

```

## Architectural Decisions Records

Here you can put your change to keep a trace of your work and decisions.

### 2023-07-24: First Init

* First init of this playbook with the bootstrap_playbook playbook by Lord Robin Crombez

### 2023-10-06: New CICD, new Images

* New CI/CD scenario name
* Molecule now use remote Docker image by Lord Robin Crombez
* Molecule now use custom Docker image in CI/CD by env vars
* New CICD with needs and optimization

### 2024-03-01: Remastered

* Imported new CICD
* Rework global on readme
* Rename of vars __

### 2024-05-19: New CI

* Added Markdown lint to the CICD
* Rework all Docker images
* Change CICD vars convention
* New workers
* Removed all automation based on branch

## Authors

* Lord Robin Crombez

## Sources

* [Ansible playbook documentation](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_reuse_playbooks.html)
* [Ansible Molecule documentation](https://molecule.readthedocs.io/)
