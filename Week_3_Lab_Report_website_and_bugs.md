#  Week 2 - Building a website 

In this lab we built a website with methods that were called on by path inputs that manipulate the backend.

---

## Which methods in your code are called?

### Methods
- **SearchEngine** method is first called to check if a port number was given and if so call handleRequest.
- **handleRequest** method is called which handles the addition of strings and searching of them.

## What the values of the relevant arguments to those methods are, and the values of any relevant fields of the class

### relevant values and arugments 
- **listOfStrings** is a relevant value and it stores all strings given by the user in the path.
- **mates** is a relevant value and it stores all the strings that match the desired string by the user.


## If those values change, how they change by the time the request is done processing

### changing values
- **listOfStrings** changes when ever the user requests to add a new value.
- **mates** changes temporarily to store the values that matches the user input.


