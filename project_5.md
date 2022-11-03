# IMPLEMENTING A CLIENT SERVER ARCHITECTURE USING MYSQL DBMS

## creating a server and client instance

### updating the server and client

`sudo apt update`

![updating](./Images/server-update.PNG)

![updating-client](./Images/updating-client.PNG)

### installing mysql server 

`sudo apt install mysql-server -y`

![installing-mysql-server](./Images/installing-mysql-server.PNG)

*opened port 3306 on my server instance inbound rule*

### configure MySQL server to allow connections from remote hosts

`sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf`

*change the bind-address to 0.0.0.0 to allow connection from remote hosts*

![configuring-remote-host](./Images/updating-bind-adress.PNG)

### creating mysql database for server

` CREATE USER 'database_name'@'IP_address' IDENTIFIED BY 'password';`

![creating-database](./Images/creating-mysql-database.PNG)

### Connecting to the server from client using the database credentials

`mysql -u database_name -h server_IP-address -p`

*-u is for username, -h is for host IP, -p is for password*

![connecting-from-client](./Images/conecting_from_client.PNG)