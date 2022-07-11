# Team Members 

* Srikar Bhavesh Desu
* Ayush Agarwal
* Aryan Gupta

# SETUP

* To install MySQL , use the following command  
```
$ sudo apt-get update  
$ sudo apt-get install mysql-server
```
* When installing the MySQL server for the first time, you will be prompted for a root password with which you can later log in. If for some reason, you aren't asked for the password during installation, try prepending the start command with sudo and provide your root password. You can then set a root password or create a new user.  
* To start MySQL use, run  
```
$ mysql -u <user_name> -p
```
* You will then be prompted for the user's password.  

* If you wish to create a new user,  
```
$ CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
```
* To grant access and modification privileges to this new user, run
```
$ GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';
$ FLUSH PRIVILEGES;
```
* Create a new database for the eCommerce website, using the following SQL command, and then set it up.
```
$ CREATE DATABASE <database_name>;
$ USE <database_name>;
```
* To initialise the database with the tables required, run
```
$ source CREATE_TABLES.sql
```
* To run the CLI ,  change your directory to the cloned folder and run the following command:
```
$ python3 python.py
```
* Meanwhile also update the required fields in the following piece of code 
```
$ conn = pymysql.connect(host="localhost",
                              user="",
                              port=3306,
                              password="",
                              database='dna',cursorclass=pymysql.cursors.DictCursor)                             
```

# INTRODUCTION

This is a CLI for a T-20 Cricket World Cup tournament where users can interact with it to insert, delete and update data in the database, and view the results of certain predefined functions that provides insight about the players and analysis of the matches played.




# FEATURES

## Insertion Functions

* ```insertmatches()``` ( To insert the details of a match in the database )                            
*  ```insertplayer()``` ( To insert the details of a player in the database )                        
* ```insertvenue()``` ( To insert the details of a venue in the database )                           
*  ```insertbatstat()``` ( To insert the batting statistics of a player in the database )             
* ```insertbowlstat()``` ( To insert the bowling statistics of a player in the database )             

## Update Functions

* ```updatematches()``` ( To update the details of an existing match in the database )  
* ```updateplayers()``` (  To update the details of an existing player in the database )  
* ```updatevenue()``` (  To update the details of an existing venue in the database  )  
* ```updatebatstat()``` ( To update the batting statistics of an existing match in the database )  
* ```updatebowlstat()``` ( To update the bowling statistics of an existing match in the database )  

## Delete Functions  


* ```deletematches()``` ( To delete a match from the database )  
* ```deleteplayers()``` ( To delete a player from the database )   
* ```deletevenues()``` ( To delete a venue from the database )  
* ```deletebatstat()``` (To delete the batting statistics of a player from the database )  
* ```deletebowlstat()``` (To delete the bowling statistics of a player from the database  )  

## Data Retrival Functions  

* ```viewmatches()``` ( To view details of all the matches in the database )                       
*  ```viewplayers()``` ( To view details of all the players in the database )                        
* ```viewvenue()``` ( To view details of all the venues in the database )                        
* ```viewbatstat()``` ( To view details of the batting statistics of all the players in the database )           
* ```viewbowlstat()``` ( To view details of the bowling statistics of all the players in the database  )             

## User functions  

* ```userfuncsplayers()``` ( Given a team id , prints all the players of that team )  
* ```userfuncsresults()``` ( Gets results of all the macthes fo a particular team id )  
* ```userfuncavg()``` ( Prints avg runs scored over all  matches )  
* ```userfuncszah()``` (Gets all the players starting with name "ZAH")  
* ```userfunchighscore()``` (Prints the highest runs scored by a player of a particular team )  








