# FSND-P5-LinuxServerConfig
Configuring a Linux server (running on amazon web services) to run catalog application using flask and postgresql 

## 1. Project IP-adress: 52.34.133.6
## 2. SSH port: 2200
## 3. public website url: http://ec2-52-34-133-6.us-west-2.compute.amazonaws.com/
## 4. A summary of installed software
- python build-dev
- python-pip
- python build-essentials
- upgrade
- apache2
- libapache2-mod-wsgi
- postgresql
- ntp
- python-setuptools
- git
- python-dev
- virtualenv
- Flask
- httplib2
- requests
- flask-seasurf
- oauth2client
- sqlalchemy
- build-dep
- python-psycopg2
- werkzeug==0.8.3
- flask==0.9
- Flask-Login==0.1.3
- fail2ban
- Glances
- unattended-upgrades

## 5. Configuration changes made
- modified ssh_config port from 22 to 2200
- added catalog.conf file to sites-available directory in apache2
- modified catalog.conf file with server the same as ip address and to point to var/www/catalog folder
- updated sudoers in vagnratfile to allow grader to have access / sudo priveleges
- changed configuration for postgres
- logged in as user grader, updated authorized keys using rsa pub key generated from ssh-keygen
- changed ssh_confing to not permit root login or password login
- changed firewall config file to allow port 2200

## 6. a list of any third-party resources used
- Udacity forums and Linux Web Server Class
- DigitalOcean, Reddit
- [Amazon faq forums] (http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#retrieving-the-public-key) - for resovling grader login issues
- [P5 Tutorial] (https://github.com/stueken/FSND-P5_Linux-Server-Configuration) - was very helpful for troubleshooting github cloning and integration
- [glances] (https://nicolargo.github.io/glances/) - to monitor development environment at aws
- fail2ban - to monitor unsuccessful login attempts
- unattended-upgrades - cron job to monitor and install packages automatically
