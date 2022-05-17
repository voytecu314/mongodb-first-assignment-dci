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

> mongo shell command: `db.info.updateOne({_id: ObjectId(62828926a649f5464f756969)},{$set:{first_name: "Steve",last_name: "Jackson",address:{building: 234, street: "Kentucky Hills", zipcode: 12753}}})
`
