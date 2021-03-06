What's this:
=========

This is to set up Keycloak with postgres with nginx reverse proxy __(https)__

1. Install docker, docker-compose

2. Install [certificates](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04)

3. Stop and remove nginx after having certs generated. ( we will have reverse proxy setup within docker-compose itself)


### Pre-requisite:

1. You need to create certificates for your domain/servername and which are prerequisites.
   

Usage:
=======

provisioning:
-------------

```

1. git clone https://github.com/aleti-pavan/nginx-keycloak-docker.git

2. cd nginx-keycloak-docker 

3. Update nginx.conf in the current directory. replace `myserver123.ukwest.cloudapp.azure.com` with your servername/domain name for which you have created certs for.

4. docker network create proxy

5. docker-compose up -d

```

You shoud now have working containers and when you put your server name in the browser, you should now see __Keycloak__ responding.

Intially you would see something like below.

![502-badgateway](images/502-badgateway.png)

If you give a minute, you should see a something like below

![welcome-keycloak.png](images/welcome-keycloak.png)


If you click on __Administration Console__ below page should appear

![login-page](images/login-page.png)

## Credentials to Login

__Credentials__ are in the .env file `username: admin; password: Pa55w0rd`

![admin-console](images/admin-console.png)


Bringing down:
-------------
```
1. docker-compose down

```

Above command should remove stop and remove working containers.


Change: (latest detail from top)
------ 


Versions(docker images):
--------

nginx:1.17.10

postgres:12-alpine 

quay.io/keycloak/keycloak:10.0.2