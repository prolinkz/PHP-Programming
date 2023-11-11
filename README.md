# PHP-Programming
1. Writing HTML and PHP
2. Comments
3. Variable
4. Data Types
 **4.1 Working With Strings
 **4.2 Working With Numbers (INT and float)
 **4.3 Working With 
5. Getting User Input
 5.1 GET and POST
 5.2 URL Parameters
6. Arrays
 6.1 Simple Arrays
  6.1.1 Using Checkboxes
 6.2 Assosiative Arrrays
7. Functions
7.1 Retun Statements
8. Statements
  8.1 If Statements
  8.2 If Else
  8.3 Swithch Statements
9. LOOPS
  9.1 While Loop
  9.2 For Loop 
10. Classes & Objects - OOPs
  10.1 Constructors
  10.2 Object Functions
  10.3 Getters & Setters
  10.4 Inheritance

[YT - freeCodeCamp](https://www.youtube.com/watch?v=OK_JCtrrv-c&t=9325s)  &nbsp;
[YT](https://www.youtube.com/watch?v=FLs6rAVQWs0)     &nbsp;
[YT _ OOPs](https://www.youtube.com/watch?v=yrFr5PMdk2A)
<hr>






## Writing HTML and PHP
 ```
<p> This is a <?php echo "awsome"; ?> Paragraph </p>
<?php echo "This is ALSO Paragraph"; ?>
```
 
## Comments

## Variable
 Variable name can be letters, numbers, or underScore prior with **$** sign. for-example <code> $FullName_01 </code>
 ```
 <?php 
 $name = "John Doe";
 echo $name;
 ?>
 ```
we can als play with numbers using varaibles to Add, multiply or divide them
 ```
 <?php 
 $num = 10;
$num= $num + 25;  // or we can use 
$num += 25;
 echo $num;
 ?>
 ```
Similarly we use the incrament for **Subsctrction -=**, **Multiplication *=** , or <code> division /= </code> 


## Data Types
  - Scaler Types (single Contins one value)    <code> $string = "new Car"; </code> <code> $int = 12345; </code>
  - Array Type (single variable name holds multi-values with it index point.  <code> $array = array() </code>
  - Object Type  <code> $object = new Car() </code>
      
  ### Working With Strings
 ```
 <?php 
 $String = "John Doe";
 echo $String;
 ?>
 ```
  
  ### Working With Numbers (INT and float)
   ```
 <?php 
 $int = "123445";
 $float = "1.24";
 ?>
 ```
  
  ### Working With Boolean
   ```
 <?php 
 $bool = true;
 ?>
 ```
We can assign one variable value to another variable like 
   ```
 <?php 
 $name = "Daniel";
 $test_name = $name;
 ?>
 ```
  
## Getting User Input
Get data from User into Input, save or return it values. First we dewclare variable to store those values. 
```
 <form action="" method="GET">
  Name: <input type="text" name="name" placeholder="Enter first name"><br>
  Age: <input type="number" name="age" placeholder="Enter your Age">

  <input type="submit">
 </form>
 Your name is <?php echo $_GET["name"] ?> <br>

 and, Your age is <?php echo $_GET["age"] ?>
```

Like we are taking input from Users of 2 numbers and add them, and print their result.
```
 $num1 = "";
 $num2 = "";
 <form action="" method="GET">
  <input type="number" name="num1" placeholder="Enter first number"><br>
  <input type="number" name="num2" placeholder="Enter Second number">

  <input type="submit">
<?php
 echo $_GET["num1"] + ["num2"]
 ?>
```

 ### GET and POST
 - **GET Method**
 ```
 <form action="" method="GET">
  <input type="text" name="firstName">

  <input type="submit">
 </form>
 <?php 
  echo $_GET["name"];
  ?>
 ```

 - **POST Method**
   POSt method is used to encrypt the value while return the required data in URL. It is a secured channel based area where to need to hide the actual data in URI link.
 ```
 <form action="" method="POST">
  <input type="password" name="password">

  <input type="submit">
 </form>
 <?php 
  echo $POST["name"];
  echo $POST["password"];
  ?>
 ```
 ### URL Parameters
 
## Arrays
array Contains multiple values under single variable. n array holds an Index number for each item value in array. We can store String, numbers with in an array. 
<code> $friends = array(); </code>

 ### Simple Arrays
  basic sytax of array is as under;
   ``` $friends = array(); ```
 To add values in arrays, we need to pass values in array. Each array item takes an index value of an array. The index start from '0 place' and the array total items could retrieve <code> n-1 </code>, where n is total iems in array.
    
    ```
    $friends = array("Daniel", "Bella", "Frida");
       echo $frineds;  //Print all values
       echo $friends[1]; //this will print index 1 value, which is Bella.
    ```

The array index start from 0 for the fisrt item, like show in table below
 
      ------ | --------|
      index  | Value   |
      ------ | --------|   
       0     | Daniel  |
       1     | Bella   |
       2     | Frida   |
      ----   | --------|
        
 We also can write array without <code> array() </code> method, but only adding <code> [] </code> parantesis in simple format in New PHP Version. Keep in mind that this approach didn't works in older verion of PHP.
 ```
 $friends = ["Daniel", "Bella", "Frida"];

```

  #### Adding Item to Arrays
  To add new item to array, we can assign it an index number to save like [4] means an index number of 4, which will be the fifth (5th) item. or we can add through **[n+1]** place where 'n' is the total length of array and **+1** means to add 1 plus index.
  ```
    $friends = array("Daniel", "Bella", "Frida");
    $friends[3] = "Johny";
      echo $friends;   
     // Now if we echo the $friends array it will contian ("Daniel", "Bella", "Frida", "Johny")

      echo $friends[3]; // print only Johny
   ```
  #### Updatuing Arrays Item value
  To edit or u[pdate the array value, we first check their index position the update like.
  ```
    $friends = array("Daniel", "Bella", "Frida");
    $friends[0] = 400;   //Now "Daniel" value chane to number 400. 
   ```


  #### Removing Item from Arrays
   To remove item from array 
   ``` jj ```

 ## Using Checkboxes
  ``` 
<?php
<form action="site.php" method="GET">
 <input type="checkbox" name=$fruits[] value="Apple"><br>
 <input type="checkbox" name=$fruits[] value="Orange"><br>
 <input type="checkbox" name=$fruits[] value="Pears"><br>
 
 <input type="submit">
</form>

$fruits; = $_GET["fruits"];  // this will return all selected items

echo $friuts[1]; // this will only print the specified item value to know either selected or not.

?>
```
  
 ### Assosiative Arrrays
   In associative array we use the <code> Key => Value </code> pair. In associative array the **key is the name** and **Pair is the value** of their age 
   ```$friends = array("Daniel=>30", "Bella=>40", "Frida=>35");```

   Check for Students exam Grades
   ```
  <?php
   $grades = array("Daniel=>A+", "Bella=>B", "Frida=>C-");
// Print the grade of Daniel, which is A+.
   echo $grades["Daniel"];

// Update Key Value for Bella
   $grades ["Bella"] = 'F';

// Print Total count numbers of items in $grades array.
   echo count($grades);

  ?>
   ```
   
## Functions
Write code at once and reuse through out the program.   The Function()performs some sort of action based, It allow us to group similar code together.  container where we write code and reuse it throughout our program.
 
   ```
 <?php
  function sayHi($name){
    echo "Hello $name <br>";
 }
   //Call Function
  sayHi("Tom");
  sayHi("Dave");
  sayHi("Olifa");
 ```
The Function() with Two or as many required parameters, like $name and $age 
   ```
 <?php
  function sayHi($name, $age){
    echo "Hello $name, your age is $age <br>";
 }
   //Call Function
  sayHi("Tom", 40);
  sayHi("Dave", 65);
  sayHi("Olifa", 45);
 ```

 ### Retun Statements
   It allow us to group similar code together.  container where we write code and reuse .
   Give a function giving information with parameters
   ```
 <?php
  function cube($num){
   return $num * $num * $num;  // Return the statement and finish process
 }
  echo cube(4);  //Call Function
 ```

## If Statements


 ### If Statements

 ```
 // IF and IF_Else statement
 $isaMale = true;
 if ($isMal){
  echo "You are Male";
 }
 ```


 ### If Else
  ```
  // IF_Else statement
   $isaMale = true;
   
    if ($isMale){
      echo "This is a Male";
      } else {
       echo "You are not male";
    )
    
  ```
  
  IF-else statement with **&& (and)** , **|| (or)** operators
  ```
  // IF and IF_Else statement
   $isaMale = true;
   $isTall = false;
    if ($isMale || $isTall){
      echo "You are Tall Male";
      } else {
       echo "You are not ";
    )
    
  ```

 ### If Else If
  ```
  // IF and IF_Else statement
 <?php

 $isaMale = true;
$isTall = false;
 if($ismale && $isTall){
   echo "You are Tall Man";
} elseif($ismale && !$isTall){
   echo "You are male but not tall";
) elseif(!$ismale && $isTall){
   echo "You are not male but tall";
) else {
   echo "You are not man not tall";
)

?>
  ```

 ### Swithch Statements

## LOOPS
 
 ### For Loop

 ### While Loop
   
## Classes & Objects - OOPs
 ###

 ### Constructors

 ### Object Functions

 ### Getters & Setters

 ### Inheritance
