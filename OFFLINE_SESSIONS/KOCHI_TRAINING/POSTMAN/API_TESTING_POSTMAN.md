---
created: 2024-07-18T09:30
updated: 2024-08-02T16:35
---


**CURD API** 

create 
update
read
delete


**REST/HTTPS methods:**

POST -  CREATE
GET - list all/ list by id  
PUT - 
PATCH 
DELETE
HEAD  - to know the headers supported by the endpoint
OPTIONS

Head - localhost:8000/api/employees
application/json
authorization


options - localhost:8000/api/employees

GET
POST
PATCH
DELETE


**RESPONSE STATUS CODE:**

SUCCESS
200 - GET
201 - POST
204  - PUT/PATCH


**CLIENT SIDE ERROR**
400  - BAD REQUEST
404 - NOT FOUND
401 - UNAUTHENTICATED 
403 - UNAUTHORISED

**SERVER SIDE ERROR**
500 -  GENERIC ERROR ON SERVER
503 -  SERVICE UNAVAILABLE
504 - BAD GATEWAY/ TIMEOUT ERROR


TRANSACTION
COMMIT
REVERT ROLLBACK

**OpenAPI/ Swagger document:**

POSTMAN:

workspace
collections


https://gorest.co.in/public/v2/users

**POSITIVE TEST CASE**
response status code - 200
size of response length > 1
check for username, mail, .. details


varad.d@gmcom
varad@d@gmexample


HTTP HEADERS:


variable at collections - collectionsvariable
varialbe at env - envrionmentalvariable


to run scripts:
- collections - 2 test cases in script
- request - per req