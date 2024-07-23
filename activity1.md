Docker Commands
------------------
 
* docker container run --name apache -d -P httpd
     -P = stands for port forwading 
     -d = Detached mode: run command in the background
 * docker ps
     This command will display a list of all running containers along with their names, IDs, and other details.
   
 * to login to the mysql container, syntax is below
     docker exec -it <container_name_or_id> mysql -u <username> -p

 * to login to the running container, syntax is below
     docker exec -it <container_name_or_id> /bin/bash

*  /var/www/html/index.html --> this is the folder where default page is located



* docker container ls
     list the running containers

* docker container stop apache

* docker container rm apache











