This is a CLI for a T-20 Cricket World Cup tournament . Users can interact with it to insert, delete and update data in the database, and view the results of certain predefined functions that provides insight about the players and analysis of the matches played.

Team Members :

1. Srikar Bhavesh Desu
2. Ayush Agarwal
3. Aryan Gupta

Setup :
You must have MySQL Server installed. To do so,
```
sudo apt-get update
sudo apt-get install mysql-server
```
When installing the MySQL server for the first time, you will be prompted for a root password with which you can later log in. If for some reason, you aren't asked for the password during installation, try prepending the start command with sudo and provide your root password. You can then set a root password or create a new user.

To start MySQL, run
```
mysql -u <user_name> -p
```
You will then be prompted for the user's password.

If you wish to create a new user,
```
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
```
To grant access and modification privileges to this new user, run
```
GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';
FLUSH PRIVILEGES;
```
Create a new database for the eCommerce website, using the following SQL command, and then set it up.
```
CREATE DATABASE <database_name>;
USE <database_name>;
```
To initialise the database with the tables required, run
```
source CREATE_TABLES.sql
```
4. To run the CLI ,  change your directory to the cloned folder and run the following command:
```
python3 python.py
```
Meanwhile also update the required fields in the following piece of code 
```
 conn = pymysql.connect(host="localhost",
                              user="",
                              port=3306,
                              password="",
                              database='dna',cursorclass=pymysql.cursors.DictCursor)                             
```

Functions :

Insertion Functions : 

1)```insertmatches()``` ( To insert the details of a match in the database ) .                         
2) ```insertplayer()``` ( To insert the details of a player in the database ) .                      
3) ```insertvenue()``` ( To insert the details of a venue in the database ) .                         
4) ```insertbatstat()``` ( To insert the batting statistics of a player in the database ) .           
5) ```insertbowlstat()``` ( To insert the bowling statistics of a player in the database ) .           

Update Functions :

1) ```updatematches()``` ( To update the details of an existing match in the database ) .
2) ```updateplayers()``` (  To update the details of an existing player in the database ) .
3) ```updatevenue()``` (  To update the details of an existing venue in the database  ) .
4) ```updatebatstat()``` ( To update the batting statistics of an existing match in the database ) .
5) ```updatebowlstat()``` ( To update the bowling statistics of an existing match in the database ) .

Delete Fucntions : 


1) ```deletematches()``` ( To delete a match from the database ) .
2) ```deleteplayers()``` ( To delete a player from the database ) .
3) ```deletevenues()``` ( To delete a venue from the database ) .
4) ```deletebatstat()``` (To delete the batting statistics of a player from the database ) .
5) ```deletebowlstat()``` (To delete the bowling statistics of a player from the database  ) .






