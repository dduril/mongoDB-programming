# MongoDB Programming

### Getting Started

- **<a href="https://www.mongodb.com/">MongoDB</a>**
- **<a href="https://docs.mongodb.com/manual/">MongoDB Docs</a>**
- **<a href="https://www.python.org/">Python</a>**
- **<a href="https://api.mongodb.com/python/current/">PyMongo</a>**

### Python

Check versions of Python and pip and get a list of installed Python packages.

	> python --version
	> pip --version
	> pip list

### Mongo Shell

Start Mongo in first terminal window:

	> C:\Development\MongoDB>mongod --dbpath=data
	
Open the Mongo Shell second terminal window:
	
	> C:\>mongo
	    
Import json file: http://media.mongodb.org/zips.json into Mongo:
	
	> C:\Program Files\MongoDB\Server\3.2\bin>mongoimport
		--db test
	    --collection zips
	    --drop
	    --file C:\Development\MongoDB\zips.json
	        
Restore a database to Mongo:
	
	> C:\>mongorestore 
		--db geodb C:\Development\MongoDB\geo



