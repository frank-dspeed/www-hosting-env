www-hosting-env
===============

A Complet WWW Hosting Envirment that creates a Directory and a Docker Container for each www Costumer and updates haproxy



# The Concept

RUNNING on HOST:
  HAPROXY
  PROFTPD
  SSHD
  DOCKER
Scripts:
etchost-docker-updater = creates etc hosts file from templates and docker

HAPROXY manager
update-haproxy -> update-haproxy-docker
create-haproxy
remove-haproxy

WWW Project Manager
create-domain = create folder /home/domain.tld mysql public_html | configure ftp /home/domain.tld | 
                start docker container dockerimages/xampp -v /home/domain.tld/public_html:/opt/lampp/htdocs/
                -v /home/domain.tld/public_html/mysql:/opt/lampp/var/mysql 
config-domain
remove-domain
  
RUNNING on CONTAINER:
preconfigured XAMPP


TODO:
Integrate Mesos
