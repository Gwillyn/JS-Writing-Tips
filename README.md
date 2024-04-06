# JS-Writing-Tips  
Check attached branches for small project demonstrations of concepts.  
This repository is a personal archive and not meant as a document to be read by the public, which is why some parts may appear disjointed, incomprehensible, or not defined properly. The point of this repository is for me to come back and review concepts I think I might need refreshing.  
  
camelCase - The first word is lowercase, every following word is uppercase...  
variables can be numbers, strings, or multiple (with [])...  
  
JS uses 0-indexing, meaning variables begin at 0 and go up (0, 1, 2, 3...). This is important to remember.  
  
There is dot.text and bracket text. Here is dot.text to call for a variable (location.text). Here is bracket[] text to call for one (```location["button text"][0]```), where the 0 indicates the first variable of the array you're calling for.  
    
Use 'document' to access html/css elements.  
```querySelector()``` is used to find a css selector as an argument and returns the first element that matches. To find h1: ```let h1 = document.querySelector("h1");```... Note that h1 is a string for the CSS element  
  
You can use let to dictate a variable, but often better is the const - it creates an error message, for example, if you happen to reassign a variable and forget. Const essentially leaves the variable unchanged forever, whereas 'let' variables can be reassigned (hence why it would create an erro message uppon reassignment).  

variable.onlcick = function // this can customize what happens when you click on the element (usually a button)  
  
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

Incrementing has a special operator: num++;  
  
There is the Math function, like Math.random() (which generates a random number from 0 (inclusive) to 1 (exclusive)) or Math.floor() (which rounds a given number down to the nearest integer)  
  
The innerHTML property allows you to access or modify the content inside an HTML element using JavaScript  
  
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

Regular expressions are used to match character combinations in strings. So, for example: 
```
  const regex = /e/;  //This will be for every 'e' found in the string.
  const regex = /e/g;  //This will find every 'e' globally (with the g flag). 
  const regex = /e/i;  //This will make the e case insensitive (so e, or E). 
```
  Regular expressions are used in some JS methods, like match() - which will find any matching results and return an array.
