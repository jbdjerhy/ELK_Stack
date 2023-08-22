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
![Picture7](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/eaa95a31-6489-49ce-8e36-acd589cb426d)
![Picture8](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/10e23e02-bd1a-479c-bc5e-2c381dd0d291)

## SSH into the Machine
- SSH into the Ubuntu server for further setup.
![Picture9](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/94a5f8c6-1a7a-4e6b-9966-93b3d48ef6be)
## Elasticsearch Installation

Add Elasticsearch GPG key
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | apt-key add -

Add Elasticsearch repository
echo "deb https://artifacts.elastic.co/packages/oss-7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list

Update package repository
apt-get update

Install Elasticsearch
apt-get install elasticsearch-oss

Enable Elasticsearch service
systemctl enable elasticsearch

Start Elasticsearch service
systemctl start elasticsearch.service

![Picture10](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/063bc752-8520-4288-96bd-e1b3a81b57aa)

Update package repository
apt-get update

Install Kibana
apt-get install kibana-oss
![Picture11](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/dcaae4a2-740e-460f-83ef-7e8dbcf9ba8d)

kibana up and running under node on port 5601
![Picture12](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/6e80bbb2-16f4-4b18-a14f-b620d4d5c20a)

Accessing Kibana through the web browser o localhost port 5601
![Picture13](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/ff9f1d67-7109-470c-bc7d-fa008cdaafa8)

Installed java dependencies and installed logstash
![Picture14](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/96485048-8470-4f09-b383-0f9979e8e247)
![Picture15](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/aef6bf97-b1d1-4c0d-a834-f99a9808cc4a)

Since logstash logs are also generated in syslog, syslogs should not be captured in logstash to avoid a loop effect which would rapdidly saturate memory ressources
![Picture16](https://github.com/jbdjerhy/ELK_Stack/assets/142699688/9b368011-05d7-463c-8f44-7290feb0c244)

