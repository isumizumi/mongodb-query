# mongodb-query

## Running:
> sudo service mongod start <br>
> connection @robomongo <br>
> mongo <br>

## Release 1
### Answer:
1. use academic
2. show collections
3. use academic
4. db.createCollection("department")
5. db.createCollection("student")
6. for(var key in db.student.findOne()){print (key, typeof key)}
7. db.department.insert([ <br>
   { <br>
      code: '001', <br>
      name: 'FPMIPA',<br>
      major: 'Education of Computer Science', <br>
   }, <br>
   {  <br>
      code: '002', <br>
      name: 'FPMIPA',<br>
      major: 'Computer Science', <br>
   }, <br>
   {  <br>
      code: '003', <br>
      name: 'FPBS', <br>
      major: 'English', <br>
   }, <br>
   {  <br>
      code: '004', <br>
      name: 'FPBS', <br>
      major: 'Germany', <br>
   }, <br>
   {  <br>
      code: '005', <br>
      name: 'FPOK', <br>
      major: 'Sport', <br>
   }, <br>
   ])
8. db.student.insert([ <br>
   {  
        studentId: '001',
        name: 'Isumi',
        address: 'Jakarta',
        department:
        {
          "$ref": "department",
          "$id": ObjectId("58b6538581ed1988a9c5f9e9"),
          "$db": "academic"
        }
   }, <br>
   {
        studentId: '002',
        name: 'Karina',
        address: 'Bandung',
        department:
        {
          "$ref": "department",
          "$id": ObjectId("58b6538581ed1988a9c5f9ea"),
          "$db": "academic"
        }
   }, <br>
   {
        studentId: '003',
        name: 'Ina',
        address: 'Bali',
        department:
        {
          "$ref": "department",
          "$id": ObjectId("58b6538581ed1988a9c5f9eb"),
          "$db": "academic"
        }
   } <br>
   ])
9.  db.getCollection('student').find({})
10. db.student.find({},{"name": 1,"address": 1}).pretty()
11. db.student.find({studentId:"003"},{"studentId": 1,"name": 1,"address":1}).pretty()
12. //Ascending: <br>
    db.student.find().sort({name:1}).pretty() <br>
    //Descending: <br>
    db.student.find().sort({name:-1}).pretty()
13. //Ascending: <br>
    db.department.find().sort({name:1}).pretty() <br>
    //Descending: <br>
    db.department.find().sort({name:-1}).pretty()
14. db.student.find({name:"Isumi"}).pretty()
