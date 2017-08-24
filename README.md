# Ubuntu Web Server                

This is a log of the details and configurations of a Ubuntu web server that was set up using Amazon Lightsail.

## Access Information

The server can be accessed using the following information listed below. However, the server will be taken down after 9/18/2017 when I pause my subscription with Amazon Lightsail.

**IP Address:** 52.40.185.170

**SSH Port:** 2200

**URL:** http://52.40.185.170/

## Software & Packages

The web server was installed using the following software:

### Server software
* Apache2 v2.4.18 (Ubuntu)
* mod_wsgi for Apache2
* PostgreSQL v9.5
* Pip v8.1.1

### Python Modules
* Flask v0.12.2
* Flask-Login v0.1.3
* SQLAlchemy v1.0.11
* Psycopg2 v2.6.1
* Oauth2client v4.1.2
* Requests v2.18.4
* Httplib2 v0.10.3

## Summary of Configurations

This Ubuntu web server was instantiated using Amazon Lightsail. The instance was loaded with Ubuntu 16.04 LTS. The uncomplicated firewall provided by Ubuntu was restricted to allow all outgoing connections and restrict incoming connections to use only SSH (port 2200), HTTP (port 80) and NTP (port 123). The remote login of the root user has been disabled for this server. An admin user was created and provided with sudo access to server files. Password authentication has been disabled, and SSH can only be access via key-based authentication. The server handles data using the PostgreSQL database. Currently, a [restaurant menu application](https://github.com/quangChe/qmenu) is being served on the server as a WSGI app.

## Resources

More information on the configuration process can be found here:

* [Setting up PostgreSQL Database on the Server](https://help.ubuntu.com/community/PostgreSQL#Basic_Server_Setup)
* [Deploying a Flask Application on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
* [Disabling Root Login Access to Server](https://www.a2hosting.com/kb/getting-started-guide/accessing-your-account/disabling-ssh-logins-for-root#Debian-and-Ubuntu)
