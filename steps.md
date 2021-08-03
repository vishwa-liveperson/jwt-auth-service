## Steps 

- C:\Users\architect>curl -X GET http://localhost:8080/users/me
    - {"timestamp":"2021-08-03T13:47:16.384+0000","status":403,"error":"Forbidden","message":"Access Denied","path":"/users/me"}
- C:\Users\architect>curl -X POST "http://localhost:8080/users/signin?username=admin&password=admin"
    - eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsImF1dGgiOlt7ImF1dGhvcml0eSI6IlJPTEVfQURNSU4ifV0sImlhdCI6MTYyNzk5ODY2OCwiZXhwIjoxNjI3OTk4OTY4fQ.O2rYs_r-zr51-k5Mu6BRehCs4wcuMyOt4YRKs2grPqI
- C:\Users\architect>curl -X GET http://localhost:8080/users/me -H "Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsImF1dGgiOlt7ImF1dGhvcml0eSI6IlJPTEVfQURNSU4ifV0sImlhdCI6MTYyNzk5ODY2OCwiZXhwIjoxNjI3OTk4OTY4fQ.O2rYs_r-zr51-k5Mu6BRehCs4wcuMyOt4YRKs2grPqI"
    - {"id":1,"username":"admin","email":"admin@email.com","roles":["ROLE_ADMIN"]}
