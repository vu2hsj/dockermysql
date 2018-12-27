# dockermysql
Docker image that can execute sql queries on volume set
# commands
# to run the mysql in -d mode and attach the volume with -v parameter
sudo docker run -d -p 3306:3306 --name my-mysql -v ~/nodeprojects/dbproject3/sql-scripts:/docker-entrypoint-initdb.d/ -e MYSQL_ROOT_PASSWORD=123 my-mysql
# go to bash
sudo docker exec -it my-mysql bash
# on mysql >
mysql -u root -p
#command mysql commands
show databases;
use <<dbname>>
show tables;
select * from <<tables>>;
