# Secure LogIn and SignUp API in PHP
[![Vishnu Sivadas](https://www.vishnusivadas.com/github/codequality.svg?style=flat)](https://github.com/VishnuSivadasVS)

A secure PHP API to manage login and signup operations. This API protects from attacks like SQL injunction and XSS. Making development work easier for developers.

## How to use?
First of all download the files DataBase.php and DataBaseConfig.php. Place it in your project folder. Go to the DataBaseConfig.php file and change the details to your database details.Now add the file DataBase.php to your project file by requiring it.
```
require "DataBase.php";
```
Simply create an object for the class DataBase.
```
$db = new DataBase();
```
Call the dbConnect() and it will return a boolean value which shows whether the database connection is success of not. 
```
$db->dbConnect();
```
Inside the current file check the condition for database connection. If it is true proceed with the rest. Check this sample code.
```
require "DataBase.php";
$db = new DataBase();
if ($db->dbConnect()) {
    //Database connection is success.
}
else{
    //Database connection is failed.
}
```
Now that the connection is success you can call the login and the signup functions. Use the object of the class DataBase and call the functions.

### Calling Login Function
Call the logIn() with the object and pass the tablename, username and password as its arguments.
```
$db->logIn($tablename, $username, $password);
```

### Calling Signup Function
Call the signUp() with the object and pass tablename, fullname, username, password and email as its arguments. You can also chnage the number of arguments as you want, but you will have to change signUp() in the DataBase class accordingly.

```
$db->signUp($tablename, $fullname, $username, $password, $email);
```

Feel free to report any issues related to this.

## Authors

* **Vishnu Sivadas** - *Developer* - [Website](https://www.vishnusivadas.com/)

Check out my other works [@VishnuSivadasVS](https://github.com/VishnuSivadasVS)
