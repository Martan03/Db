# PHP Database class

## Usage:
First you need to require database class:
`require_once("Db.php");`
Then you can connect to the database. This is example on localhost:
`Db::connect("127.0.0.1", "database_name", "root", "");`
And now you can start using your database. This is example of getting all rows and columns from database:
```
Db::queryAll("
    SELECT *
    FROM your_database
");
```

## List of features
- Connecting to database using PDO connection
- Executing query and:
    - Getting number of effected rows
    - Getting all effected rows
    - Getting first effected row
    - Getting first effected row's first column
- Easy insert and update functions to use
