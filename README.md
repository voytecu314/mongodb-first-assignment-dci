# mongodb-first-assignment-dci

## 1. Create a database “persons”

> mongo shell command: `use persons` 

## 2. Create a collection “info” in “persons” database

> mongo shell command: `db.createCollection("info")`

## 3. Insert a person to the collection “info” with the following structure:
```javascript
{
“address”: {
    “building”: “1007”,
    “street”: “Morris Park Ave”,
    “zipcode”: “10462”
},
“first_name”: “Tom”,
“last_name”: “Joe”,
“age”: 39
}
```

> mongo shell command: `db.info.insertOne({address: {building: 1007, street: "Morrisson Park Ave", zipcode:10462},first_name:"Tom", last_name:"Joe", age: 39})`

## 4. Insert 4 persons to the collection “info” with the above structure

> mongo shell command: `db.info.insertMany([{address: {building: 1007, street: "Morrisson Park Ave", zipcode:10462},first_name:"Tom", last_name:"Joe", age: 39}, {address:{building: 1037, street: "Morrisson Park Ave", zipcode:10462},first_name:"Ben", last_name:"Furry", age: 29}, {address: {building: 100, street: "Deen Avenue", zipcode:11262},first_name:"Garry", last_name:"Lost", age: 33}, {address:{building: 10, street: "Dark Matter St.", zipcode:14466},first_name:"Allan", last_name:"Starsky", age: 49},{address: {building: 17, street: "Toy Valley", zipcode:19492},first_name:"Aik", last_name:"McCarry", age: 28}, {address:{building: 1307, street: "Geaverier Street", zipcode:13967},first_name:"John", last_name:"Cooper", age: 43}])
`

## 5. Update 1st persons address and his/her first_name

> mongo shell command: `db.info.updateOne({_id: ObjectId("62828926a649f5464f756969")},{$set:{first_name: "Steve",last_name: "Jackson",address:{building: 234, street: "Kentucky Hills", zipcode: 12753}}})
`

## 6. Add new row to the 1st person: “gender”: “male/female”

mongo shell command: `db.info.updateOne({_id: ObjectId("62828926a649f5464f756969")},{$set:{gender: "male"}})
`

## 7. Delete from the collection “info” 4th person’s document

mongo shell command: `db.info.deleteOne({_id: ObjectId("62828b86a649f5464f75696c")})
`

## 8. Find document(s) from “info” collection who’s age is greater than 30

mongo shell command: `db.info.find( { age: { $gt: 30 } } )
`

## 9. Find document(s) from “info” collection who’s age is less than 30

mongo shell command: `db.info.find( { age: { $lt: 30 } } )
`

## 10. Find document(s) from “info” collection who’s age is less than 30 but more than 20



## 11. Rename 2nd person’s name



## 12. Display the fields address, first_name, last_name but exclude the field age for all the documents in the collection “info”
