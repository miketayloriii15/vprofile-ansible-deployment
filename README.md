vProfile — DevOps Automation with Ansible

This project demonstrates how to automate the provisioning and deployment of a full Java web application stack using Ansible.
It sets up all the components needed to run a production-ready Spring MVC application:

Application server: Apache Tomcat (for running the Java/Spring app)

Database: MySQL 8 (with an included SQL dump to restore the app’s schema and data)

Caching: Memcached (active & standby)

Messaging: RabbitMQ (for asynchronous communication)

Search engine: Elasticsearch (for indexing and search features)

The Ansible playbooks handle installing and configuring each service, deploying the application WAR file, and preparing the environment automatically — so you can go from a fresh server to a running app with one command.

This project is useful for learning and showcasing DevOps skills such as:

Infrastructure as Code (IaC) with Ansible

Automated deployments of Java/Spring applications

Setting up a complete multi-tier stack (database, cache, message broker, search, app server)

Managing Linux services and environment-specific templates

Prerequisites

JDK 17 or 21

Maven 3.9

MySQL 8

Technologies

Spring MVC

Spring Security

Spring Data JPA

Maven

JSP

Tomcat

MySQL

Memcached

RabbitMQ

Elasticsearch

Database

This project uses a MySQL database.
A database dump file is included at:

/src/main/resources/db_backup.sql


To import it:

mysql -u <user_name> -p accounts < db_backup.sql


To load it into your MySQL server, run:

mysql -u <user_name> -p accounts < db_backup.sql
