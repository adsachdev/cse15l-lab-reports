# Lab Report - 2
April 22, 2024

## Part 1

* `ChatServer.java` code:
  ```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {

    String output = ""; 

    public String handleRequest(URI url) {
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            if (parameters[0].contains("s=") && parameters[1].contains("user=")) {
                String[] messageParam = parameters[0].split("=");
                String message = messageParam[1]; 
                String[] userParam = parameters[1].split("=");
                String user = userParam[1];

                output = output + String.format("%s : %s" + "\n", user, message);
                return output; 
            } 
            return "Add message!";
        }
        return "404 Not Found!";
    }

}

/** Code copied from NumberServer.java in CSE15L lab */
class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
  ```
* Screenshots using `/add-message`:
  a. ![webpage1](http://url/a.png)
    1. The `handleRequest` method was called to check the url and print the message onto the webpage. 
    2. The argument to the method was a url. An important class field is one called `output` which currently stores an empty string.
    3. The `output` value was changed from an empty string `""` to the first message of type `user : message`.
  b. ![webpage2](http://url/a.png)
    1. The `handleRequest` method was called to check the url and print the message onto the webpage. 
    2. The argument to the method was a url. An important class field is `output` which currently stores the first message that was printed. 
    3. The `output` value was changed from the first message of type `user : message` to now print two messages of the type `user : message`.

 ---

## Part 2

1. My computer - `ls` with absolute path to private key
  ![privatekey]()
2. `ieng6` machine - `ls` with absolute path to public key
  ![publickey]()
3. Login to `ieng6` without password
  ![login]()

---

## Part 3

Something new I learned it lab that I didn't know before was how to run server from a remote computer. I also learned to log into my `ieng6` account for the first time and then login without requiring a password. 


