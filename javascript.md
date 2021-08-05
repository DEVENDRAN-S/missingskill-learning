# JAVASCRIPT
### HISTORY
* it was invented in the year of 1995.
* Earlier designed for mocha/ecma script
* it was donated to ECMA to create a standard implementation
* new js is based on ECMA script.
* javascript `=` java `+` live script
###  BROWSER
* Chrome.
* Brave.
* Mozilla firefox.
* Edge.
* Opera.
* Safari.
### VARIABLES
 * Variables are containers
 * category 
    - primitive
    - non primitive .
### TECH DEBT 
 * **(+)**
    - add when all the variables are numbers
    - concat when one of the variable is string
* **===** identity/ typecheck.
* **null** it is an object in javascript.
### CONTROL STATEMENT
 * if-else -often used 
 * for - abstractions
 * switch - better way available in js 
 * while - normal use
 * do  while - normal use

### OPERATORS
* Arithmetic
* logical
* comparison
* bitwise
* ternary
 #### Aritmetic 
#### `*,-,/,%,++,--,+`

#### Comparison operator
#### `===,==,!=,>,<,<=,>=`
 
#### Ternary operator
#### `<condition>?<if_true>:<if_false>`
#### Logical Operator

#### `&&` : 
  if both the values are true returns output
#### `||`: 
if one of the value is true returns output
####  `!` : 
if gives negative value of expression.
#### Truth Table

#### NOT 
| exp1 | NOT |
|------|-----|
| true | false|
| false| true|

#### AND & OR            
| exp1 | exp2 | AND | OR |
|------|------|------|----|
| true | true | true | true|
| true | false| false| true|
|false | true | false| true|
|false | false| false| false|

### TYPES OF VARIABLE
**Primitive** 
  - It is copy by value /pass by value
  - **Example:-**
     Assingment copy in college.
  - string 
  - boolean
  - number
  - undefined
  - symbol
  - null

**Non primitive**
  - It is copy by reference/pass by reference
  - **Example:-**
   Debit cards linked to account
  - object
  - array 

### VARIABLE DECLARATION
  * Variable declared by:
    -  var (ES5)
    -  let  (ES6)
    -  const (ES6)

**VAR**
 * Functional scope
 * Redeclared
 * hoisted
 * Reassigned
 * local variable override global variable
 ***example:***
     ```javascript
      deva();
      var deva= function(){
      console.log("devendran");//hoisted
     }//devendran
     ```
**LET**
* lexical scope
* Reassigned
* not redeclared
* not hoisted
***example:***
  ```javascript
  let value;
  value=function(a){
    console.log(a);
  }
  value(10);//10
  ```
**CONST**
* lexical scope
*  not reassigned
* not redeclared
* not hoisted
***example:***
  ```javascript
  const num =30;
  console.log("1", num);//30
  function outer() {
  console.log("2", num);//30
  function inner() {
  let num = 70;
  console.log("3",num)//70
  }
  inner();
  }
  outer();
  ```
| var                    | let    |   const  |
| -----------------------| ------ |-------|
| It is introduced in ES5 |It is introduced in ES6     |  It is introduced in ES6    |
| It's get hoisted        |  It doesn't get hoisted    |It doesn't hoisted       |
| It has finctional scope | It has lexical/block scope |  It has lexical/block scope    |
| It can be redeclare and reassign/reinitialize | It's only reassign/reinitialize |  It can't be redeclare and reassign/reinitialize    |
|It can be first declare after that assign|It can be first declare after that assign|  It declare and assigne at a time|
### SCOPE
**Functional scope**
 each program or application can be called as functional scope(global functional scope). And each function within program have their own functinal scope(local functional scope) which exist untill the function exists. `var` keyword has functional scope
   - ***global variable*** :global variables are variables defined outside of functions,can be used by any functions and anywhere.
   - ***local variable***: local variables defined within functions,can only be used within that function in which they are defined its scope exist only within that function not outside of that function.

**Lexical Scope/Block Scope** :
it  starts and end with curly braces `{ }`also called block is lexical scope/block scope. Any variable that exist only inside curly braces `{ }` has lexical scope.let and const have lexical scope.`let and const` has lexical scope.
  ```javascript
  var a=10;
  var b=5;
  var b="ok";
  console.log(1,a+b);//10ok
  a=20;//functional scope
  function hello(){
    console.log(2,a);//undefined
    var a=3;//lexical scope
  }
  hello();
  console.log(3,a);//20
  a=10;
  console.log(4,a);//10
  ```
### FUNCTIONS
  * in javascript everything is an object.
  * whenever we access any  function it will show the return value
  * properties
    - container
    - hoisted
    - global and local scope
    - object
    - override
  
    **syntax:**
     ```javascript
    function <name>(){
      console.log()
    }
    name();
    ```
    **Test check**
     ```javascript
    !!name && (typeof name === "function") && name();
     ```

  #### FIRST CALSS FUNCTION
   * function can be assigned to a variable
   * function can be return from another function  
#### DECLARATION 
   * function is declared directly.
   * it has been hoisted.
   **syntax:**
  ```javascript
    deva(a);
    function deva(a){
      console.log(a)
    }
  ```
  #### ASSIGNMENT
  * function is asssigned to another variable.
  * function is not hoisted.
  **syntax:**
  ```javascript
     var value=function(a){
      console.log(a)
    }
    value(a);
  ```
  #### HIGHER ORDER FUNCTION
   * function which takes function  as input and /or function as output is known as higher  order function.
   ```javascript
    const print1=function(value){
    console.log('printing=',value);
     }
    const outside=function(param){
    c=a*b;
    print1(c);
    }
    var a=10;
    var b=23;
   outside(print1);//printing=230
   ```
  #### PURE FUNCTION
   * function which takes input as one parameter and return the output of  same parameter it is known as pure function.
   ```javascript
   function add(a,b){
     c=a+b;
   }
   add(1,3)//4
   ```
  #### IIFE/SEF
   * function can act like private method,if we want function to be executed only once we use iife and then it's return value can be assing to variable.
   `function expression:(function(){})()`
   ```javascript
    const print1=function(value){
    console.log('printing=',value);
     }
    const outside=(function(next){
    console.log("initialisation....")
    function hello(value){
        next(value);
    }
    return hello;
    })(print1)

    outside(10);//initialisation.....printing=10
   ```
  #### INLINE FUNCTION
   *   function in which the values are assigned directly is known as inline function.
   ```javascript
      function func1(a){
        console.log(a);
      }
      func1(10);
   ```
  #### ARROW FUNCTION
   * in function assignment you can elimate the function by using arrow function `=>`
   ```javascript
     var value = a => console.log(a);
     // Is same as below

     var value = function(a){
     return console.log(a);
     };
   ```
### OBJECT
 * Object literal (mostly used)
 * new Object Object constructor
 * Function constructor (Function converted to Object prototype)
 * Object.create() (not really used)
 * Object has 
   - keys
   - values
 * this keyword
   - this keyword is used to  get current function, class and object when we use normal function it is act as a window object.
### STRING
 * split
   - it is used to split the string into delimeter
 * toLowerCase()
   - it is used to convert the string in lower case
 * toUpperCase()
   - it is used to convert the string in upper case 
 * trim()
   - it is used remove the white space from both the side of string
 * length
   - length is property used to check how many char present in the string

 * replace(src,tag)
   - it is used to replace the string what we want to replace 
### ARRAY
 * isArray()
   - It is check the value is array or not
 * length()
   - It is a property of array to check the last value of idex value of an array
 * join()
   - It is used delimeter and convert array to string
 * map()
   - It is iterate the array value and return new array
 * orEach()
   - It is iterate ther array value
 * includes()
   - It is used to check the key(index) present in array or not
 * indexOf()
   - It is used to check the key(index) present in array or not
 * filter()
   - It is used to filter the value
 * concat()
   - It is used to add two or more arrays 
 * push()
   - It is add the value in end of an array
 * pop()
   - It is remove the value in end of an array
 * unshift()
   - It is add the value in begining of an array
 * shift ()
   - It is remove the value in begining of the array