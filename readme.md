### SQL vs NoSQL
* DataBase = DataBase
* Table = Collections
* Record(row) = Documents
* Column = Field

### Connection to MongoDB compass
* New Connection
* Cluster -> CONNECT -> Connect your application -> copy the string in "Connection String Only"
* Connect via Python
	- mongodb://gjgg:a1b2c3@mflix-wo96r.gcp.mongodb.net/test?retryWrites=true&w=majority


### 以下才是正確上傳csv.file指令, Altas 藏在 "Command and Line Tools" 裡面
範例程式碼：
mongoimport --host mflix-shard-0/mflix-shard-00-00-wo96r.gcp.mongodb.net:27017,mflix-shard-00-01-wo96r.gcp.mongodb.net:27017,mflix-shard-00-02-wo96r.gcp.mongodb.net:27017 --ssl --username gjgg --password <PASSWORD> --authenticationDatabase admin --db <DATABASE> --collection <COLLECTION> --type <FILETYPE> --file <FILENAME>


mongoimport --host mflix-shard-0/mflix-shard-00-00-wo96r.gcp.mongodb.net:27017,mflix-shard-00-01-wo96r.gcp.mongodb.net:27017,mflix-shard-00-02-wo96r.gcp.mongodb.net:27017 --ssl --username gjgg --password a1b2c3 --authenticationDatabase admin --db mflix --collection movie_initial --type csv --headerline --file movies_initial.csv