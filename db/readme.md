# a database for beam test
* db_lib.py: contains various methods to read/write the db, it also has a 
interactive shell to operate the db.

* db.py: is a wrapper of db_lib.py which allows callable methods from other scripts

# example
To initilize the database
```
./db.py init	
```
which will create both the 'irradiation' and 'SiPM_test' tables.

To see what fields are contained, use
```
./db.py query
```

To insert a test record, use the 'insert' command:
```
./db.py  insert --SiPM_id 1 --test_type IV --source led --begin_time '20230615 15:00:00' --end_time '20230615 16:00:00' --annealing no --filename test
```
