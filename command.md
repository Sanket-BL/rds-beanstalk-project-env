# Commands Used

## Connect EC2
ssh -i key.pem ec2-user@<public-ip>

## Install MySQL Client
sudo dnf install mariadb105 -y

## Connect to RDS
mysql -h <endpoint> -u admin -p

## SQL Commands
CREATE DATABASE internship;
USE internship;
CREATE TABLE users (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(50)
);
INSERT INTO users(name) VALUES ('Sanket');
SELECT * FROM users;
