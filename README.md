# mongodb-query

# MongoBD Query
#### 1. Membuat database academic
```
use academic
```
#### 2. Menampilkan semua collection dan data dalam database
```
show collections
```
#### 3. Membuat atau mengaktifkan database
```
use <nama database>
```
#### 4. Membuat collection departement
```
db.department.insert({
  "code" : 12345,
  "name" : "XXX",
  "major" : "XXX1"})
```
#### 5. Membuat collection student
```
db.student.insert({
  "studentId" : A1,
  "name" : "yoma",
  "address" : "jakarta",
  "department" :{
    "$ref" : "department",
    "$id" : ObjectId("589013683a1464bcced014de")    
  }})
```
#### 6. Melihat struktur collection student
```
 db.student.find();
```
#### 7. Menginputkan 5 data ke dalam collection department
```
db.department.insert([{
  "code" : 12345,
  "name" : "Komputer",
  "major" : "TI"},
  {
  "code" : 12346,
  "name" : "Komputer",
  "major" : "SI"},
  {
  "code" : 12347,
  "name" : "Komputer",
  "major" : "MI"},
  {
  "code" : 12348,
  "name" : "Komputer",
  "major" : "AKA"},
  {
  "code" : 12349,
  "name" : "Komputer",
  "major" : "ELEKT"}])
```
#### 8. Menginputkan 3 data ke dalam collection student beserta reference ke department
```
db.student.insert([{
  "studentId" : "A0",
  "name" : "yona",
  "address" : "jakarta",
  "department" :{
    "$ref" : "department",
    "$id" : ObjectId("589013683a1464bcced014de")    
  }},
  {"studentId" : "A2",
  "name" : "yomi",
  "address" : "bandung",
  "department" :{
    "$ref" : "department",
    "$id" : ObjectId("589013683a1464bcced014e1")    
  }},
    {"studentId" : "A3",
  "name" : "yoga",
  "address" : "bali",
  "department" :{
    "$ref" : "department",
    "$id" : ObjectId("589013683a1464bcced014df")    
  }}
  ])
```
#### 9. Melihat isi collection student
```
db.student.find();
```
#### 10. Menamplikan key name dan address dalam collection student
```

```
