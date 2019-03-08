# Linux Server Configuration Project
## Purpose
Udacily Full Stack Web Developer Nanodegree Program project #3 by [Slava Balashov](mailto:slavabal@gmail.com ).

## Description
The purpose of this project is to set up a Linux server with good security settings, a running web server, and deploy Item Catalog project from earlier in the NanoDegree

## Settings and configuration

### Server settings

- IP Address `54.68.5.36`

- SSH Port `2200` 

### Software installed (for the project)

- Apache Web Server (+mod_wsgi)
- PostgreSQL 
- Python3
    - Flask 
    - SQLAlchemy
    - oauth2 libraries (connectivity to Google)

## Server access and security configuration
- `grader` account added to the server (SSH key + password are submitted with the project)
- `grader` is given `sudo` access
- key-based authentication is enforced
- `root` remove login disabled
- PostgreSQL allows local connections only (using `catalog` user)
- Flash app and sources are not under www/html Apache folder

### Firewall configuration
Allow rules:
- `SSH (2200)`
- `WWW (80)`
- `NTP (123)`

### SSH Access
Connect to the server:  `ssh grader@54.68.5.36 -p 2200 -i <ssh-key-file>`

### Web server access
Open [`http://54.68.5.36`](http://54.68.5.36) with your browser

Note: Item Catalog project profides sufficient functionality, but there are limitation related to Google-based OAuth for servers with "public IP addresses" or with dymanic IP-DNS services (noip.com and others). 
There are personal plans to use this system to add domain name to it and play with the follow-up scalability improvements for Item Catalog project. 
Exciting as they are and hopefully to be implemented soon enough that falls out of the scope of this project. :)

## Resources
- [Udacity ND materials](https://www.udacity.com/)
- [Flask Deployment Options](http://flask.pocoo.org/docs/1.0/deploying/)
- [Flask Hello World App with Apache WSGI](https://www.bogotobogo.com/python/Flask/Python_Flask_HelloWorld_App_with_Apache_WSGI_Ubuntu14.php)
- [StackOverflow](https://stackoverflow.com/)
- [Amazon Lightsail Docs](https://lightsail.aws.amazon.com/ls/docs/en/all)