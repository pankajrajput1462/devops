sudo apt install mysql-server
sudo mysql

### To change the root user’s authentication method to one that uses a password. 

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Pankaj@1234';


$ sudo mysql -u root -p

CREATE USER 'pankoo'@'localhost' IDENTIFIED BY 'Pankoo@123';
