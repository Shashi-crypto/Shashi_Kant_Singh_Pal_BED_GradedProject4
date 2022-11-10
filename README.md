### Guide to run the program

1.)Create a DB employee_mgmt in Mysql by running the below command.

create database employee_mgmt;

2.) Run the Employee Program

3.)Open Postman
   
4.) In Authorization tab select basic Auth and in username fill Shashi and Password admin


Now you may proceed with the below commands:


1. Role

POST: http://localhost:8080/restapi/role

Body: Raw JSON

{
"name":"SUPER_USER"
}

2. User

POST :http://localhost:8080/restapi/user

Body: Raw JSON

{
"username":"temp",
"password":"12345",
"roles":[{
"id":2,
"name":"USER"
}]
}


3. Add Employee by only Admin as Shashi is Admin and Anu is User

POST  http://localhost:8080/restapi/employees

Body: Raw JSON

{
"firstName":"gl",
"lastName":"postman",
"email":"postman@gamil.com"
}


4. Get All Employees

GET http://localhost:8080/restapi/employees



5. Get Employee on ID

GET http://localhost:8080/restapi/employees/1


6. Update an Employee


PUT http://localhost:8080/restapi/employees

{
"id":1,
"firstName":"postman",
"lastName":"postman",
"email":"postman@gamil.com"
}

7. Delete an Employee


Delete http://localhost:8080/restapi/employees/1


8. Search

Get http://localhost:8080/restapi/employees/search/Shashi


9.  list all employee records sorted on their first name


Get http://localhost:8080/restapi/employees/sort?order="asc"  

Get http://localhost:8080/restapi/employees/sort?order="desc"
