# MongoDB Notes



## Show databases

<u>You need to be connected as admin</u> 

` show dbs`

__output__ : 

```mongo output
> show dbs
admin       0.000GB
config      0.000GB
local       0.000GB
weather_ai  0.000GB
```



## Select a db

` use weather_ai`

__output__ : 

```
> use weather_ai
switched to db weather_ai
```



## Show Collections

` show collections `

__ouput__ :

```
cards
logs
mqttconfigurations
```



## Select all document in a collection



`db.collection.find().pretty()`



__example__:



```json
 	> db.cards.find().pretty()
{
	"_id" : ObjectId("5b32e0f1ef20d83f73d54253"),
	"pieces" : [
		{
			"parameters" : [
				{
					"value" : "100",
					"_id" : ObjectId("5b32e0f1ef20d83f73d54251"),
					"name" : "Temperature"
				}
			],
			"_id" : ObjectId("5b32e0f1ef20d83f73d54252")
		}
	],
	"date" : ISODate("2018-06-27T00:57:21.014Z"),
	"cardId" : "E3:23:12:44:22",
	"__v" : 0
}
```



## Insert a new document

` db.collection.insert({"key": "value"})`

__example__:

```
db.mqttconfigurations.insert({ "card": "E3:23:12:44:22", "parameter": "Temperature"})
```

