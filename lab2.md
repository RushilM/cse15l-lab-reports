# Lab Report 2
## Part 1
**StringServer Webserver Code**

StringServer.java is below:

```
import java.io.IOException;
import java.net.URI;

interface URLHandler {
    String handleRequest(URI url);
}

class StringHandler implements URLHandler {
    private StringBuilder message = new StringBuilder();
    private int messageCounter = 0;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String query = url.getQuery();
            String[] parameters = query.split("s=");
            if (parameters.length == 2) {
                messageCounter++;
                String newMessage = parameters[1];
                message.append(messageCounter + ". " + newMessage + "\n");
                return message.toString();
            }
        }
        return "404 Not Found!";
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new StringHandler());
    }
}

```
**Screenshot 1: Adding the message "Hello"**
![Alt text](Lab2CSE15LScreenshot1.png)

The method 'handleRequest(URI url)' in the 'StringHandler' class. 

Relevant argurments are the URI object which will get the path '/add-message' and the query string 's=Hello'

The resulting field changes is that 'message' gets updated to "1.Hello\n". Also the messageCounter is incremented to reflect that 'Hello' is the first message. 



![Alt text](Lab2CSE15LScreenshot2.png)

The method 'handleRequest(URI url)' in the 'StringHandler' class. 

Relevant argurments are the URI object which will get the path '/add-message' and the query string 's=How%20are%20you'

Note: the %20 represents the hexadecimal value for the space character. 

The resulting field changes is that 'message' gets updated to "1. Hello\n2.How+are+you\n". Also the messageCounter is incremented to reflect that 'How are you' is the second message. 
