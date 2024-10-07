# Cooking Competition Management System
### Databases ECE NTUA 2023-2024
#### Graded 92.1/100

## Team's Members 



 
 
 **Afroditi Marianthi Chlapani [github](https://github.com/aphrochl)**  
 **Kyriaki Karatzouni [github](https://github.com/ntua-el20634)**  

---

## Project Overview

This project implements a **Database Management System** for a competitive cooking show. The system manages recipes, ingredients, equipment, cooks, judges, and competition episodes. Each recipe includes detailed steps, required ingredients, nutritional information, and cooking equipment. The system automates the selection of recipes and judges for each episode and tracks scores, which are later used to evaluate cooks. Advanced SQL queries are used to provide insights into cook performance, episode statistics, and nutritional data.

Key features:
- Recipe management with difficulty levels, meal types, and nutritional info.
- Cooks and judges management with expertise and professional ranking.
- Automatic competition episode management and score tracking.
- Complex SQL queries to gather insights on cooks, episodes, and recipes.
- Database design with ER diagrams, relational schemas, and optimized queries.

---

 # Contents


- [Prerequisites](#Prerequisites)
- [Database](#Database)




## Prerequisites

Steps to install/run the prerequisites for our database: 

We worked with MySQL to create the database and we used MySQL Workbench and phpMyAdmin interchangeably. 

1. Install XAMPP:

   https://www.apachefriends.org/download.html

   
   After opening it, enable the Apache and MySQL Modules.

   If you get the below error:
   Problem detected!
   Port 3306 in use by "Unable to open process"!
   MySQL WILL NOT start without the configured ports free!
   You need to uninstall/disable/reconfigure the blocking application
   or reconfigure MySQL and the Control Panel to listen on a different port

   1) Stop the Apache Server from XAMPP Control Panel (if running)
   2) Now open XAMPP Control Panel => Config (Top Right) => MySQL and change the Main Port to 3307 => Save => Save
   3) Click Config of MySQL (From Control Panel only) => my.ini and then Change all the occurrences of 3306 to 3307 (Search using ctrl + F and replace all)
   4) Click Config of Apache (From Control Panel only) => config.inc.php and then search for the line: $cfg['Servers'][$i]['host'] = '127.0.0.1';. Now add this below the line you found: $cfg['Servers'][$i]['port'] = '3307';

Now, you are good to go. Also note that you would have to change port for all your projects to 3307 for them to work properly. For eg: from $servername = "localhost"; to $servername = "localhost:3307"; in the database config file of your project.


2. Open phpMyAdmin at:

   http://localhost/phpmyadmin/

   and you’re ready to create a new database!


Alternatively, you can use MySQL Workbench: 

2. Install MySQL Workbench at:

   https://dev.mysql.com/downloads/workbench/

   After creating a connection (i.e. ”Username” as “root”), you should specify the “Port” as “3306”, or whichever port you have on the MySQL Module in XAMPP. 

   After opening the connection, again you’re ready to create a new database! Specifically, ours. 

 





## Database

Steps to create/populate the database: 

#### Git clone

You can git clone our github repository for easy access to the SQL files, by firstly going to the desired directory in the command line: 

```sh
cd C:\Desktop 
```

and executing: 

```sh
git clone https://github.com/aphrochl/Databases2023-2024.git
```

#### Database Creation

Then, you can create a new database in either phpMyAdmin or MySQL Workbench and  import the SQL files in the following order: 
  
1. [schema.sql](https://github.com/aphrochl/Databases2023-2024/blob/main/database/schema.sql)

2. [initial_data.sql](https://github.com/aphrochl/Databases2023-2024/blob/main/database/initial_data.sql)

3. [indexes.sql](https://github.com/aphrochl/Databases2023-2024/blob/main/database/indexes.sql)

  You can execute the queries either one by one (preferably) or as a whole, in the file:
 
4. [queries.sql](https://github.com/aphrochl/Databases2023-2024/blob/main/database/queries.sql )
