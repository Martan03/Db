# PHP Database class

## Usage:
First you need to require database class:
```php
require_once("Db.php");
```
Then you can connect to the database. This is example on localhost:
```php
if (Db::connect("127.0.0.1", "database_name", "root", ""))
{
    header("Location: 500");
    exit;
}
```
And now you can start using your database. This is example of getting all rows and columns from database:
```php
Db::queryAll("
    SELECT *
    FROM your_database
    WHERE name = ?
", array("name"));
```

## List of features
- Connecting to database using PDO connection
- Executing query and:
    - Getting number of effected rows
    - Getting all effected rows
    - Getting first effected row
    - Getting first effected row's first column
- Easy to use insert and update functions
