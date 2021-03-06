This Repository contains all information related to the ISBOS JavaScript Club which meets Fridays at 3:30pm


The club's main goal is to look at programming in the real world (games, software...etc) and to do so, we examine basic programming concepts which are listed below:

# Variables
Just as in math, a variable is a symbol that references a different value over time. There are a variety of types that a variable can hold. These include, integers (5), strings ("hi"), booleans (True) and a few other types that we haven't covered as a group yet. Javascript is a dynamically typed language which means that to create a variable, you can just use the same keyword (var) for all variables. You do not have to specify the type that the variable holds. Instead, the computer will infer what type it is holding. 
Variables are central to programming. It is important that a variable has a good name. You should be able to look at someones code and understand it just based off the variable names. In this club, when we talk about variables, we say "They hold something". 


#### Code Examples

```javascript
var x; //This creates a variable called x
x = 5; //This sets the value of variable x to 5
var t = "hi"; //This creates a variable called t and sets its value to "hi"
r = "sam"; //This is invalid because a variable named r hasn't been created yet
```

#### More Information

[w3 Schools JavaScript Data Types] (http://www.w3schools.com/js/js_datatypes.asp)
[w3 Schools JavaScript Variable] (http://www.w3schools.com/js/js_variables.asp)
[w3 Schools JavaScript Variable Scope] (http://www.w3schools.com/js/js_variables.asp)


# Functions
A function is a block of code that is designed to complete a task. A function must be defined somewhere in your code. This means that you tell the computer what a function does. When you "call" a function, it jumps to the section of code where a function is defined, executes it, and then returns back to the original place in the code that was being exectuted. A function accepts arguments when it is called. These arguments are variables that the function then does something with.

#### Code Examples

```javascript
//This function accepts two numbers as its arguments, adds them together and then returns the sum
function sum(num1, num2) {
	var s = num1 + num2;
	return s; // s holds the sum of num1 and num2
}

//This function accepts two numbers as its arguments and returns the larger of the two.
function max(x, y) {
	if(x > y) {
		return x;
	}
	else {
		return y;
	}
}

//This function accepts three numbers as its arguments and returns the average of the three.
function avg(a, b, c) {
	var sum = a + b + c;
	var avg = sum / 3;
	return avg;
}

var t = sum(5,6); //This is how you would "call" the sum function. This will add 5 and 6, and store the result in variable t
var a = 4; // Stores 4 in variable a
var b = 6; // Stores 6 in variable b
var c = sum(a,b); //This will add the values of the variables a and b, and store the result in c. Since a holds 4 and b holds 6, c will hold 10

t = max(a, b); // This will store the max of whats in variable a and variable b, in variable t. You'll notice we used t earlier, and now are overwrtiing the value
a = sum(max(4,5), avg(4,5,6)); // This is an example of how you can "nest" functions. That is, you can put a function call in place of another functions argument.
// To evaluate nested functions, you must work from the inside out. 
// Lets start with max(4,5). This will return the value 5.
// Next, look at avg(4,5,6). This will return 5.
// Finally, replace the function calls with the appropriate return values so now you have a = sum(5,5)
// This is easy! You know this function returns 10


var invalid = sum(4, 5, 6, 6, 8, 9); // This is an invalid function call. We are calling the sum function and passing 6 arguments. However, the sum function is defined to only accept 2 arguments.

var a = 5;
var b = 6;
var c = 7;
a = max(max(max(1, a), 3), c); // This will return 7. Again, start from the inside and work out:
// max(1,a) will compare 1 and 5 so it will return 5
// max (5, 3) will compare 5 and 3 so it will return 5
// max (5, c) will compare 5 and 7 so it will return 7

```

#### More Information

[w3 Schools JavaScript functions] (http://www.w3schools.com/js/js_functions.asp)


# Conditionals

A conditional statement compares values and has defined operations depending on the comparison. Valid comparisons are "==" (equal), "!=" (not equal), ">" (greater than), "<" (less than), ">=" (greater than or equal to), "<=" (less than or equal to). You can combine conditions using "&&" (and), "||" (or), and "!" (not). The condition goes between () and the code to be evaluated as a result goes between {}. See examples below:

#### Code Examples

```javascript
var a = 10;
if(a > 10) {
	a = a + 5; // set a to 5 more than its original value
}

var b = "Sam";
if(b == "Jim") { //If the value inside variable b is the string "Jim", do something
	return 1;
} else if(b == "John") { // If the value was not Jim, check if its "John". If so, do something
	return 2;
} else { // If the value wasn't caught by either of the above if statements, do something
	return 3;
}

var name = "Kim";
var age = 28;
if(name == "Kim" || age == 14) { // If the name variable holds "Kim" OR if the age variable holds 14, do something
	return "Success";
} else { // If the above condition (in the if statement) wasn't true, do something
	return "Failure";
}

```

#### More Information

[w3 Schools JavaScript Conditionals] (http://www.w3schools.com/js/js_comparisons.asp)

# Loops
Loops are methods of repeating a chunk of code. This may repeat for a certain number of times, or until a condition is no longer true. The two major types of loops are while loops and for loops. 

## While Loop
The purpose of a while loop is to repeat a chunk of code WHILE a condition is true. Once the condtion is no longer true, the loop breaks and the program continues executing whatever code is below the loop.

#### Code Examples

```javascript
var a = 10;
while (a > 0) {
	console.log(a); //print the value of a
}	a = a - 1; // Set a to one less than its previous value
console.log("Done");
//The above while loop first checks the condition (a > 0). Since a is 10, and 10 > 0, this condition is true and the computer looks at the code inside the {} brackets. 
//It prints out the value of a (10) to the screen and then sets a to 9 (a = 10 - 1). 
//Next, it checks the conditional again, but this time with the updated value of a, which is now 9. Since 9 > 0, it completes the code inside the {} brackets again. 
//This loop repeats again and again until a reaches a value where the condition, a > 0 is not true. 
//Once this happens, the code after the {} brackets will execute and "Done" will be printed to the screen.
```



