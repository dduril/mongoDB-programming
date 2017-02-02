# MongoDB Programming


#### Starting Mongo and Importing Dataset

	# command prompt #1 - launch mongod
	C:\development\mongodb>mongod --dbpath=data

	# command prompt #2 - import dataset
	C:\Program Files\MongoDB\Server\3.2\bin>mongoimport
		--db usdata
		--collection cityinfo
		--drop
		--file C:\Development\MongoDB\zips.json
    
	# command prompt #3 - launch shell
	C:\>mongo

#### Show Databases

	> show dbs

#### Select Database *usdata*

	> use usdata

#### Show Collections for *usdata*
	> show collections

#### A few queries

	> db.cityinfo.find()
	> db.cityinfo.find().limit(10)
	> db.cityinfo.count()
	> db.cityinfo.find({ pop: { $lt: 5000 }})

#### Using a cursor

	> cacitycursor = db.cityinfo.find({ $and: [{ state: "CA" }, { pop: { $gt: 10000, $lt: 100000 }}]})
	> cacitycursor.count()
	> cacitycursor.next()