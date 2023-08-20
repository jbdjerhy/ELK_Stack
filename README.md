# ELK_Stack
# Project Title: ELK Stack Installation and Configuration for Log Analysis

## Project Description
This project aims to set up and configure an ELK stack (Elasticsearch, Logstash, and Kibana) on an Ubuntu server for log analysis and monitoring purposes.

## Project Scope
- Provision an Ubuntu Server using Vagrant and Git for Windows.
- Install and configure Elasticsearch.
- Install and configure Kibana.
- Set up Java dependencies.
- Install and configure Logstash.
- Ensure proper log management and avoid log loop issues.

## Objectives
1. **Provision Ubuntu Server:** Create and configure an Ubuntu Server VM using Vagrant and Git for Windows.
2. **Elasticsearch Setup:** Install and configure Elasticsearch for log indexing and storage.
3. **Kibana Installation:** Install Kibana for log visualization and analysis.
4. **Java Dependencies:** Install Java dependencies required for the ELK stack.
5. **Logstash Installation:** Install and configure Logstash to collect and process logs.
6. **Log Management:** Implement proper log management strategies to prevent log loop issues.

## Resources
- Ubuntu Server VM provisioned using Vagrant.
- Elasticsearch, Kibana, and Logstash software packages.
- Java dependencies.

## Timeline
- Define timelines for each objective, specifying start and end dates.

## Budget
- Allocate a budget for any additional resources or licenses if required.

## Team
- Identify team members responsible for each aspect of the project.

## Deliverables
- Ubuntu Server VM provisioned and configured.
- Elasticsearch installed and configured.
- Kibana installed and running on port 5601.
- Java dependencies installed.
- Logstash installed and configured.
- Log management strategies implemented.

# ELK Stack Installation and Configuration

## Ubuntu Server Setup
- Used Vagrant and Git for Windows to install a test Ubuntu Server.

## SSH into the Machine
- SSH into the Ubuntu server for further setup.

## Elasticsearch Installation
```bash
# Add Elasticsearch GPG key
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | apt-key add -

# Add Elasticsearch repository
echo "deb https://artifacts.elastic.co/packages/oss-7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list

# Update package repository
apt-get update

# Install Elasticsearch
apt-get install elasticsearch-oss

# Enable Elasticsearch service
systemctl enable elasticsearch

# Start Elasticsearch service
systemctl start elasticsearch.service

# Update package repository
apt-get update

# Install Kibana
apt-get install kibana-oss



