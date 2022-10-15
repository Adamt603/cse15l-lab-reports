#  Week 2 - Building a website 

In this lab we built a website with methods that were called on by path inputs that manipulate the backend.

---

## Which methods in your code are called?

### Methods
- **SearchEngine** method is first called to check if a port number was given and if so call handleRequest.
- **handleRequest** method is called which handles the addition of strings and searching of them.

---

## What the values of the relevant arguments to those methods are, and the values of any relevant fields of the class?

### relevant values and arugments 
- **listOfStrings** is a relevant value and it stores all strings given by the user in the path.
- **mates** is a relevant value and it stores all the strings that match the desired string by the user.

---

## If those values change, how they change by the time the request is done processing?

### changing values
- **listOfStrings** changes when ever the user requests to add a new value.
- **mates** changes temporarily to store the values that matches the user input.

---

![image](Imagies/lab2and3/2.png)
![image](Imagies/lab2and3/3.png)
![image](Imagies/lab2and3/4.png)
![image](Imagies/lab2and3/5.png)
![image](Imagies/lab2and3/6.png)
![image](Imagies/lab2and3/7.png)
![image](Imagies/lab2and3/8.png)
![image](Imagies/lab2and3/9.png)

```
import java.util.*;
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler{
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    ArrayList<String> listOfStrings = new ArrayList<String>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Number: %d", num);
        } 
        else if (url.getPath().equals("/increment")) {
            num += 1;
            return String.format("Number incremented!");
        } 
        // else if (url.getPath().equals("/search")) {
        //     System.out.println("Path: " + url.getPath());
        //     if (url.getPath().contains("/search")) {
        //         String[] parameters = url.getQuery().split("=");
        //         if (parameters[0].equals("s")) {
        //             StringBuilder eb = new StringBuilder();
        //             for (String e: listOfStrings){
        //                 eb.append(e);
        //                 eb.append(",\t");
        //             }
        //             return String.format("Strings added: %s", eb.toString());
        //         }
        //     }
        //     return "404 Not Found!";
        // }
        else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    listOfStrings.add(parameters[1]);
                    return String.format("String added is %s", listOfStrings.get(num++));
                }
            }
            else if (url.getPath().contains("/search")) {
                ArrayList<String> matches = new ArrayList<String>();
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    int index1 = listOfStrings.indexOf(parameters[1]);
                    for (String all: listOfStrings){
                        if (all.contains(parameters[1])){
                            matches.add(all);
                        }
                    }
                    String k[] = matches.toArray(new String[matches.size()]);
                    String str = Arrays.toString(k);
                    return String.format("Strings added: %s", str);
                }
                return "404 Not Found!";
            }
        return "404 Not Found!";
```


#  Week 3 - Bug fixing