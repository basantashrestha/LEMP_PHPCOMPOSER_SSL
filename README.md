Implements Nginx, PHP, PHP COMPOSER, MARIA DB, PHP MYADMIN AND SSL  

Make following changes in /etc/hosts on the host system. Use DNS on real system.  
127.0.0.1       sample.localhost.localdomain            sample  


#Clone Repository  
git clone https://github.com/basantashrestha/LEMP_PHPCOMPOSER_SSL.git  
cd LEMP_PHPCOMPOSER_SSL  
docker-compose up -d  


#Check on Browser  
http://sample.localhost.localdomain  
or  
http://sample.localhost.localdomain/info.php  


#To add virtual host. Make corresponding changes. Exmple is given below  
cp -r app/vhost-sample app/example.com  
cp config/nginx/vhost-sample.conf to config/nginx/example.com.conf  

##Access Phpmyadmin   
http://sample.localhost.localdomain:8181  
username: root  
password: your_password(This should be the mysql password you provide on docker-compose.yml file)   


##For SSL we need to work with real domain . The following video can be helpful   . 

https://www.youtube.com/watch?v=m9aa7xqX67c  

