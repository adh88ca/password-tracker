# password-tracker
application to store passwords in a database and have them easily retrievable.

##Purpose
To be able to store passwords from websites, servers, and applications.

Please Note:
This is not currently a secure way of storing your passwords, as it stores them in plain text in a mysql table.
This script also assumes .my.cnf is configured to connect to your database

##Commandline Help:
passwords - main command
eg:

###First Argument:
add - add a password to a group

list - list passwords in a group

remove - remove a password from a group

newgroup - create a new group

listgroup - list groups

removegroup - delete a group

###Second Argument

group - name of table or group of passwords

###Third Argument (dependant on first argument)

name

##Queries

add - insert into 'group' ('name','desc','pass') values (name,desc,pass)

list - select * from 'group' where 'name'=""

remove - delete from 'group' where 'name'=""

newgroup - create table 'group' (id int auto increment not null, name varchar(50) not null, desc varchar(255), password varchar(20) not null primary key(id))

listgroup - show tables;

removegroup - drop table 'group'

