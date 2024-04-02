# JS-Writing-Tips  
Check attached branches for small project demonstrations of concepts.  
This repository is a personal archive and not meant as a document to be read by the public, which is why some parts may appear disjointed, incomprehensible, or not defined properly. The point of this repository is for me to come back and review concepts I think I might need refreshing.  
  
camelCase - The first word is lowercase, every following word is uppercase...  
variables can be numbers, strings, or multiple (with [])...  
  
JS uses 0-indexing, meaning variables begin at 0 and go up (0, 1, 2, 3...). This is important to remember.  
  
There is dot.text and bracket text. Here is dot.text to call for a variable (location.text). Here is bracket[] text to call for one (location["button text"][0]), where the 0 indicates the first variable of the array you're calling for.  
    
Use 'document' to access html/css elements.  
querySelector() is used to find a css selector as an argument and returns the first element that matches. To find h1: let h1 = document.querySelector("h1");... Note that h1 is a string for the CSS element  
  
You can use let to dictate a variable, but often better is the const - it creates an error message, for example, if you happen to reassign a variable and forget. Const essentially leaves the variable unchanged forever, whereas 'let' variables can be reassigned (hence why it would create an erro message uppon reassignment).  

variable.onlcick = function // this can customize what happens when you click on the element (usually a button)  
  
// This is a function:
function buyHealth() {  
  
}  

  
