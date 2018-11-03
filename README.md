#### ip address
18.191.254.176

#### url
http://18.191.254.176.xip.io

#### software and configurations:

update & upgrade server packages and software via sudo apt-get commands

sudo nano /etc/ssh/sshd_config to change ssh port and disallow root login

create grader user and assign super user privleges

software + config changes made:

installed apache2
pulled in libraries to run wsgi:
sudo apt-get install libapache2-mod-wsgi python-dev
sudo a2enmod wsgi

added catalog directory to /var/www
installed & setup postgresql for application db
install python-psycopg2 for python pg interaction
installed git
pulled application repository into /catalog

changed owner of /var/www/catalog to ubuntu
installed python-pip to run pip commands
installed virtualenv to run pip commands via python virtual environment
installed application dependencies
setup db with models.py

added sudo nano /etc/apache2/sites-available/catalog.conf to configure virtual host via port 80
deactivated default.conf
added catalog.wsgi file to serve application

modified js origins and authorized redirects to include production url
modified client_secrets.json file to achieve the same
modified path in application file in order for client_secrets to load.

restart apache

set firewall to allow ports 80, 123 and 2200

#### resources used in service of project completion:
https://www.digitalocean.com/community/tutorials/how-to-configure-the-apache-web-server-on-an-ubuntu-or-debian-vps

https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps#step-four-%E2%80%93-configure-and-enable-a-new-virtual-host

http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi/
