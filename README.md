# Linux Server Configuration

## Project Overview



The purpose of this project was to:
> take a baseline installation of a Linux server and prepare it to host your web applications. You will secure your server from a number of attack vectors, install and configure a database server, and deploy one of your existing web applications onto it

[Udacity Project Overview](https://classroom.udacity.com/nanodegrees/nd004/parts/ab002e9a-b26c-43a4-8460-dc4c4b11c379/modules/357367901175462/lessons/3573679011239847/concepts/36124987540923)

This project required the deployment of the previously created "Catalog" project and deploy it on AWS Lightsail Ubuntu Server. In addition, security measures were implemented to harden the server against common attacks.

### Flora Catalog Web Application

Server IP Address - 18.220.144.46

SSH Port - 2200

URL - http://ec2-18-220-144-46.us-east-2.compute.amazonaws.com

## Summary

Resources used for initial setup of server - [Digital Ocean](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-12-04#step-one—root-login)

### User Management

1. Create Amazon Lightsail Instance
2. Create newuser grader and provide access to Sudo - [UDACITY](https://classroom.udacity.com/nanodegrees/nd004/parts/ab002e9a-b26c-43a4-8460-dc4c4b11c379/modules/357367901175461/lessons/4331066009/concepts/48010894700923)
2. Create SSH Private Keys using Git Bash and Upload to AWS - [GIT](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key)
3. Disable remote login of `root` user. - [Media Temple](https://mediatemple.net/community/products/dv/204643810/how-do-i-disable-ssh-login-for-the-root-user)

### Security

1. Configure firewall to only allow SSH, HTTP, and NTP connections.[UBUNTU WIKI](https://wiki.ubuntu.com/UncomplicatedFirewall#Basic_Usage) and [UDACITY](https://classroom.udacity.com/nanodegrees/nd004/parts/ab002e9a-b26c-43a4-8460-dc4c4b11c379/modules/357367901175461/lessons/4331066009/concepts/48010894980923)
2. Key-based SSH authentication is enforced. - [Techoism](http://www.techoism.com/configure-ssh-key-based-authentication-linux-server/)
3. All system packages have been updated to most recent versions. - [UDACITY](https://classroom.udacity.com/nanodegrees/nd004/parts/ab002e9a-b26c-43a4-8460-dc4c4b11c379/modules/357367901175461/lessons/4331066009/concepts/48010894520923)
4. Is SSH hosted on non-default port? - [UBUNTU Help](https://help.ubuntu.com/community/SSH/OpenSSH/Configuring)

### Application Functionality

This application is setup to serve the Floral Catalog website on port 80. It uses a Postgresql database and properly functions as designed. In addition, it uses Google for authentication to enable adds, edits, and deletes the website data.

### Major Software Installed

Web Server: Apache2 - [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-16-04)
Database Management: Postgresql - [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04)
Web Framework: Flask - [Profit Bricks](https://devops.profitbricks.com/tutorials/deploy-a-flask-application-on-ubuntu-1404/)

Git was installed in order to clone the Catalog project.

In addition, many packages were installed in order for the project.py(later changed to __init__.py) application to run. Such as, SQL Alchemy, httplib2, and oauth2client.

### Basic Overview of Installation

1. Install Apache2 -[Digital OCean](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-16-04)
2. Install mod_wsgi to serve Python application.- [Flask](http://flask.pocoo.org/docs/0.10/deploying/mod_wsgi/)
3. Install and Setup Postgresql - [Digital Ocean](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04)
4. Install and deploy Flask - [Flask](https://devops.profitbricks.com/tutorials/deploy-a-flask-application-on-ubuntu-1404/)
