# UG_Web

Docker Files to setup nginx & mariaDB 

Build : 
docker build -t ugweb/lemp .

Runtime :
docker run -d --name=ugweb -v /home/vivek/DockerFS/ugweblemp/www/:/var/www/ -v /home/vivek/DockerFS/ugweblemp/mysql:/var/lib/mysql -v /home/vivek/DockerFS/ugweblemp/php:/var/log/php -p 80:80 ugweb/lemp

Connect :
docker exec -it ugweb bash
docker run --name ugweb --rm -i -t ugweb/lemp bash