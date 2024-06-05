# Javascript Writing Tips  
Check attached branches for small project demonstrations of concepts.  
This repository is a personal archive for concepts and parts I've learned in javascript. Many parts may appear disjointed, incomprehensible, or not defined properly. This is because it is meant for me to read, so I can quickly get refreshed on ideas I learned previosuly. The point of this repository is for me to come back and review concepts. 
# Javascript 
Javascript is a dynamically typed OOP language.
# Cases
camelCase - The first word is lowercase, every following word is uppercase...  
variables can be numbers, strings, or multiple (with [])...  
# Javascript Indexing 
JS uses 0-indexing, meaning variables begin at 0 and go up (0, 1, 2, 3...). This is important to remember.  
  
There is dot.text and bracket text. Here is dot.text to call for a variable (location.text). Here is bracket[] text to call for one (```location["button text"][0]```), where the 0 indicates the first variable of the array you're calling for.  
# Syntax
```.split()``` takes a string and splits it into an array of strings. What you put into the method counts as the separator, or multiple separators (with commas).  
```.map()``` takes a callback function as its first argument, and goes through each element of the attached array with that function in mind.  
```.filter()``` takes a callback function as its first argument and needs to return a boolean value.  
# Accessing external files (HTML, CSS, etc)
Use 'document' to access html/css elements.  
```querySelector()``` is used to find a css selector as an argument and returns the first element that matches. To find h1: ```let h1 = document.querySelector("h1");```... Note that h1 is a string for the CSS element  
The innerHTML property allows you to access or modify the content inside an HTML element using JavaScript  
# Variables
You can use let to dictate a variable, but often better is the const - it creates an error message, for example, if you happen to reassign a variable and forget. Const essentially leaves the variable unchanged forever, whereas 'let' variables can be reassigned (hence why it would create an erro message uppon reassignment).  

variable.onlcick = function // this can customize what happens when you click on the element (usually a button)  
# Functions 
This is a function:
```
function buyHealth() {  
  gold = gold - 10;  
  health = health + 10;  
}
``` 
  
Compound Assignment can be used in the above function to make the code cleaner, turning gold = gold - 10 into gold -= 10. (See below code).  
  ```
  function buyHealth() {  
  gold -= 10;  
  health += 10;  
}  
```
# Incrementing
Incrementing has a special operator: num++;  
  
There is the Math function, like Math.random() (which generates a random number from 0 (inclusive) to 1 (exclusive)) or Math.floor() (which rounds a given number down to the nearest integer)  
    
# Ternary Operators
Ternary operators can be used to make sure negative values are not returned.      
    ```condition ? expressionIfTrue : expressionIfFalse```  // this is like a one-line if/else statement     
                
                 **if-else statement**  
                  if (s > 0) {  
                    return s   
                    } else {  
                    return default_s  
                    }  
  
                  **ternary operator**  
                  return s > 0 ? s : default_s  
# Loops!
A ```while``` loop accepts a condition, and will run the code in the block up until the condition is no longer true.  
A ```for``` loop runs for a specified number of times.
    Syntax: ```for (a;b;c)``` where (a) is the initial expression and is executed only once and sets up the variable, (b) is the condition and is evaluated at every beginning of the loop (the loop will continue as long as this is true), and (c) is the final expression and is executed at the end of every loop.  
    A ```for``` loop example is this:  
```
    for (let i = 0; i < sArray.length; i++) {  
      if (!['+', '-', ' '].includes(sArray[i])) {  
        bArray.push(sArray[i]);  
      }  
    }  // this loop checks if i is below the length of sArray, and gets increased by 1. if the (+, -, ' ') are NOT (!) included in sArray with intiger i, it is pushed into bArray.
```
# REGEX (Regular Expressions)
Regular expressions are used to match character combinations in strings. So, for example: 
```
  const regex = /e/;  //This will be for every 'e' found in the string.
  const regex = /e/g;  //This will find every 'e' globally (with the g flag). 
  const regex = /e/i;  //This will make the e case insensitive (so e, or E). 
```
  Regular expressions are used in some JS methods, like match() - which will find any matching results and return an array.  
  ```[]``` will create character classes, so ```/fr[e3][e3]``` will match free, or fr33, or fre3, or fr3e.  
  the alternate operator ```|``` allows different things. ```/million|billion|trillion/``` will match million, or billion, or trillion.  
  ```\s``` is a meta tag for checking spaces. So ```/\shello\s/``` will check for spaces before and after 'hello'.  
#Template Literals
  Template literals ```${}``` can allow for direct insertions of variable values in strings. Instead of quotes for the string, you must use back-ticks. The below example would output the string "My name is Gwillyn.":  
      ```  
      const name = "Gwillyn"  
      const myNameText = `My name is ${name}.`  
      ```  
# NodeLists
A NodeList allows you to access the elements using bracket notation and acts like an array.  

Much like the onclick function, another interactive addition is the event listener.    
# Compare Callback functions
Compare callback functions are   
  
# Returns 
using ```return``` at the end of statements, functions, etc (especially if statements) is important if you want the function to stop there and not compute the rest of the code in it.  

# Call Stacks
stack is a data structure where items are stored in a last-in-first-out (LIFO) manner. The last book you add to a stack of books is the first book you can take off.   
  The 'call stack' is a collection of function calls stored in a stack structure, like the books. Added functions are put on the top of the stack. It is removed from the top/end of the stack when it is returned.  
  in this array: 	  
```
const callStack = [  
'a(): returns "Gwillyn " + b()',  
'b(): returns "is " + c()',  
'c(): returns "cool"'  ];
```
The a() function is at the bottom or beginning of the stack, which calls b() in the middle, which calls c() at the tippy top. When c() executes, it returns the string "cool", and is popped off/removed from the top of the stack.  
Recursive functions calls itself over and over. Therefore, it is a good idea to write a _base case_ to allow for the function to stop calling itself, and it is a good idea to write it first. The recursive case is where the function calls itself. When writing the recursive case, you need to ask **1.** What is the base case? and **2.** What is the least work needed to get closer to the base case?  

# Spread operator 
```(...)``` allows for an iterable to be expanded where functions or elements are expected. 

# Sorting Algorithms 
```.sort()``` can sort in itself, but it is somewhat limiting as it converts ints to strings which can complicate things. To get past this, passing a function into the ```.sort()``` method. This function will return a number which will determine how the elements are sorted. If the number is positive, return a before b, if it is negative return b before a, and the return of zero will keep the current placements. This can all be done with a single return statement with a subtraction of a and b.
```
const sortValues = inputValues.sort((a, b) => {
    return a - b;
  });
```
  
**Bubble Sort:**  
Through an array, iterating through every element and bubbling the (in the example) smallest number toward the start and the bigger number to the end.  
```
const bubbleSort = (list) => {  
  for (let i = 0; i < list.length; i++) {  
    for (let j = 0; j < list.length - 1; j++) {  
      if (list[j] > list[j + 1]) {  
        const temp = list[j];  
        list[j] = list[j + 1];  
        list[j + 1] = temp;  
      }  
    }
return list
}
```
**Selection Sort:**  
Through an array, it relies on tracking the index of the smallest value.   
```
const selectionSort = (list) => {
  for (let i = 0; i < list.length; i++) {
    let minimumIndex = i;
    for (let j = i + 1; j < list.length; j++) {
      if (list[j] < list[minimumIndex]) {
        minimumIndex = j;
      }
    }
    const temp = list[i];
    list[i] = list[minimumIndex];
    list[minimumIndex] = temp;
  }
  return list
}
```
**Insertion Sort:**  
Through an array, it builds up an assorted array from the beginning of the list.  
starts at the beginning of the list (the first element is already sorted), and uses a ```while``` loop.  
This ```while``` loop needs two conditions met: it shoult not run beyond the beginning of the array, and the loop should not run after the finding of a value smaller than the current one.  
```
const insertionSort = (list) => {
  for (let i = 1; i < list.length; i++) {
    const currentValue = list[i];
    let j = i - 1;
    while (j >= 0 && list[j] > currentValue) {
      list[j + 1] = list[j];
      j--;
    }
    list[j + 1] = currentValue;
  }
  return list
}
```



