# Simple DevOps Project

This Repository is a collection of Implementation documents. 

### Purpose:
By following this repository you can able to setup a DevOps CI/CD Pipeline using
- git
- Jenkins
- Maven
- Ansible
- Docker &
- Kubernetes

Steps on CI/CD Operation:
1. From Jenkins Add git and github account
2. Add publish over ssh on jenkins
3. From ansible server download docker also along with python ansible
4. Create Docker file that has FROM tomcat and COPY war file to /usr/lib/local/tomcat/
5. Create ansible playbook that runs docker commands for image creation using docker built of docker file and docker push to docker hub and docker rmi of that created image
6. Publish everytime there is changes on github script or every build to ANSIBLE Server with ansible playbook
7. Use exec command on publish over ssh jenkins to run ansible playbook to update docker hub every changes on github repo
8. From Docker server, pull newly updated repo on docker hub and exec docker run
