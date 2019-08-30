# FseFinal

1. The project is placed in the Desktop - C:\Users\Admin\Desktop\Project

	Java Project-FullStackDev 
	Angular Project - my-app
2. The code is placed in the git path  :


http://172.18.2.18/gnagappriya/Fullstack/tree/master


URLs to access the Rest Service:

1. http://localhost:8082/taskManager/addParentTask
2. http://localhost:8082/taskManager/addTask
3. http://localhost:8082/taskManager/getAllTasks
4. http://localhost:8082/taskManager/suspendTask
5. http://localhost:8082/taskManager/updateTask
6. http://localhost:8082/taskManager/addProject
7. http://localhost:8082/taskManager/addUser
8. http://localhost:8082/taskManager/getAllUsers
9. http://localhost:8082/taskManager/deleteUser
10.http://localhost:8082/taskManager/updateUser
11.http://localhost:8082/taskManager/getAllProjects
12.http://localhost:8082/taskManager/getAllParentTasks

Database Scripts:

create database fse;
use fse;

CREATE TABLE parenttasktable(
  parentid int(10) NOT NULL  AUTO_INCREMENT PRIMARY KEY, 
parenttask varchar(50)) ;

create table ProjectTable(
projectid int(10)  AUTO_INCREMENT PRIMARY KEY,
project varchar(100),
startdate date,
enddate date,
priority varchar(10)
);

CREATE TABLE  TaskTable ( 
taskid int(10) NOT NULL AUTO_INCREMENT PRIMARY KEY, 
enddate date, 
priority varchar(10) , 
startdate date,
task varchar(50) ,
parentid int (10),
taskstatus varchar(50) ,
projectid int(10),
FOREIGN KEY(parentid) 
REFERENCES  parenttaskTable(parentid),
FOREIGN KEY(projectid) 
REFERENCES  ProjectTable(projectid)
);
CREATE TABLE  UsersTable ( 
userid int(10) NOT NULL AUTO_INCREMENT PRIMARY KEY, 
firstname varchar(50), 
lastname varchar(50) , 
employeeid varchar(50), 
projectid int(10) ,
taskid int (10)
);

