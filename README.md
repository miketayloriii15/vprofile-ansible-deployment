vProfile — Multi-Tier Web Application DevOps Automation

This project is my baseline DevOps environment for future work.
From my Windows laptop, I use Vagrant and Ansible to automatically create and configure a multi-tier social media web application stack.
It’s a real-world style setup that helped me learn how to build and run complex systems locally before moving to the cloud.

🌐 Project Architecture
Application & Services

NGINX – reverse proxy & load balancer

Apache Tomcat – runs the Spring MVC Java application

RabbitMQ – message broker for asynchronous communication

Memcached – caching layer

MySQL – relational database for the app’s data

Automation & Tools

Vagrant – VM creation and lifecycle management

VirtualBox – hypervisor used to run the VMs

Ansible – automated provisioning and configuration

Git Bash – CLI used on Windows to run Vagrant/Ansible commands

Git / GitHub – version control and project hosting

🏗️ VM Layout
VM Name	Role	Main Services
lb01	Load balancer	NGINX
app01	Application server	Tomcat, Maven
db01	Database	MySQL / MariaDB
mc01	Caching	Memcached
rmq01	Messaging	RabbitMQ
es01	Search (optional / for learning)	Elasticsearch

All of these machines are created locally by Vagrant + VirtualBox, then fully provisioned by Ansible playbooks.

🚀 Why I Built This

Local multi-tier web app setup — practice building a full stack on my laptop before deploying to cloud environments.

Real-world baseline — this environment will be the foundation for my upcoming DevOps and cloud projects.

VM automation — create, configure, and deploy a full environment automatically from Windows.

Hands-on DevOps learning — Infrastructure as Code, provisioning, Linux service management, and app deployment.

⚙️ How to Run

Install Vagrant
 and VirtualBox
 on Windows.

Install Git Bash
 (if not already installed).

Clone the repo:

git clone https://github.com/yourusername/vprofile-ansible-deployment.git
cd vprofile-ansible-deployment


Start the whole stack:

vagrant up


Vagrant spins up the VMs in VirtualBox.

Ansible automatically provisions each VM (installs NGINX, Tomcat, RabbitMQ, Memcached, MySQL, deploys the app, etc.).

When the playbooks finish, the application is up and running locally behind the NGINX load balancer.

🛠 Technologies

Spring MVC / Spring Security / Spring Data JPA

Tomcat

MySQL

Memcached

RabbitMQ

Elasticsearch

Maven

NGINX

Vagrant / Ansible / VirtualBox

🗄 Database

A MySQL dump is included:

/src/main/resources/db_backup.sql


To restore manually (if needed):

mysql -u <user_name> -p accounts < db_backup.sql

✨ Summary

This repository shows a real-world DevOps workflow — creating a multi-tier Java/Spring web application stack using Vagrant, VirtualBox, and Ansible, all automated from a Windows machine.
It’s my personal baseline for future projects and a hands-on example of provisioning, deployment, and infrastructure automation.
