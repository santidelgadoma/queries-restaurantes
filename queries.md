13
```javascript
db.restaurants.find({"cuisine":{$not:/^American/},"grades.grade":"A","borough":"Brooklyn"},{"cuisine":1,"grades.grade":1,"borough":1}).sort({"cuisine":-1})
```
14
```javascript
db.restaurants.find({"name":/^Wil/},{"name":1,"restaurant_id":1,"borough":1,"cuisine":1})
```
15
```javascript
db.restaurants.find({"name":/ces$/},{"name":1,"restaurant_id":1,"borough":1,"cuisine":1})
```
16
```javascript
db.restaurants.find({"name":/Reg/},{"name":1,"restaurant_id":1,"borough":1,"cuisine":1})
```
17
```javascript
db.restaurants.find({"borough":"Bronx","cuisine":{$in:["Chinese","American "]}})
```
18
```javascript
db.restaurants.find({"borough":{$in:["Brooklyn","Bronx","Queens","Staten Island"]}},{"restaurant_id":1,"name":1,"borough":1,"cuisine":1})
```
19
```javascript
db.restaurants.find({"borough":{$nin:["Brooklyn","Bronx","Queens","Staten Island"]}},{"restaurant_id":1,"name":1,"borough":1,"cuisine":1})
```
20
```javascript
db.restaurants.find({"grades.score":{$lt:10}},{"restaurant_id":1,"name":1,"borough":1,"cuisine":1,"grades.score":1})
```
21
```javascript
db.restaurants.find({"name":/Wil/,"cuisine":{$nin:["Chinese","American "]}},{"restaurant_id":1,"name":1,"borough":1,"cuisine":1,"grades.score":1})
```
22
```javascript
db.restaurants.find({ "grades" : { $elemMatch : {"score" : 11,"date": ISODate("2014-08-11T00:00:00Z")} } , "grades.grade" : "A"},{ "restaurant_id": 1, name:1, "grades.grade":1})
```
23
```javascript
db.restaurants.find({ "grades" : { $elemMatch : {"score" : 9,"date": ISODate("2014-08-11T00:00:00Z")} } , "grades.1.grade" : "A"},{ "restaurant_id": 1, name:1, "grades.grade":1})
```
24
```javascript
db.restaurants.find({"address.cord.1":{$gte:42,$lt:52}},{"restaurant_id":1,"name":1,"address.street":1,"address.zipcode":1})
```
25
```javascript
db.restaurants.find().sort({"name":1})
```
26
```javascript
db.restaurants.find().sort({"name":-1})
```
27
```javascript

db.restaurants.find({}, {cuisine:1, borough:1}).sort({  borough: -1, cuisine: 1})
```
28
```javascript
db.restaurants.find({"address.street":{$exists:false}},{"name":1,"address.street":1}
```
29
```javascript
db.restaurants.find({"address.coord":{$type:"double"}})
```
30
```javascript
db.restaurants.find({"grades.score":{$lte:7}},{"restaurant_id":1,"name":1,"grades.score":1})
```
31
```javascript
db.restaurants.find({"name":/mon/},{"name":1,"borough":1,"address.coord":1,"cuisine":1})
```
32
```javascript
db.restaurants.find({"name":/^Mad/},{"name":1,"borough":1,"address.coord":1,"cuisine":1})
```
