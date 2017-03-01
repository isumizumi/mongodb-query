# mongodb-query

## Release 1
### Answer:
1. use academic
2. show collections
3. db
4. db.createCollection("department")
5. db.createCollection("student")
6. db.getCollection('student').find({})
7. db.department.insert([
   {
      code: '001',
      name: 'FPMIPA',
      major: 'Education of Computer Science',
   },
   {
      code: '002',
      name: 'FPMIPA',
      major: 'Computer Science',
   },
   {
      code: '003',
      name: 'FPBS',
      major: 'English',
   },
   {
      code: '004',
      name: 'FPBS',
      major: 'Germany',
   },
   {
      code: '005',
      name: 'FPOK',
      major: 'Sport',
   },
])
8. db.student.insert([
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
   },
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
   },
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
   }
])
9.  db.getCollection('student').find({})
10. 
