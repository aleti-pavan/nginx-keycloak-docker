What's this:
=========

This is to set up Keycloak with postgres with nginx reverse proxy __(https)__

1. Install docker, docker-compose

2. Install [certificates](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04)

3. Stop and remove nginx after having certs generated.

4. `git clone https://github.com/aleti-pavan/nginx-keycloak-docker.git`

5. cd nginx-keycloak-docker

6. Update nginx.conf in the directory. replace __testserver.westus.cloudapp.azure.com__ with your servername/domain name for which you have created certs for.

7. docker-compose up -d.

8. You shoud now have working containers and when you put your server name in the browser, you should now see __Keycload__ responding.


### Pre-requisite:

1. You need to create certificates for your domain/servername and which are prerequisites.


Usage:
=======

provisioning:
-------------

1. `git clone https://github.com/aleti-pavan/nginx-keycloak-docker.git`

2. cd nginx-keycloak-docker

3. Update nginx.conf in the directory. replace __testserver.westus.cloudapp.azure.com__ with your servername/domain name for which you have created certs for.

4. docker-compose up -d.

Bringing down:
-------------

1. docker-compose down.

Above command should remove stop and remove working containers.



Change: (latest detail from top)
------ 


Versions:
--------
