# Unit 12 Submission File: Web Development 
​
---
## Questions 
​
Before you work through the questions below, please creat a new file and record your answers there. This will be your homework deliverable.
​
## HTTP Requests and Responses
​
Answer the following questions about the HTTP request and response process.
​
​
1. What type of architecture does the HTTP request and response process occur in?
​
​
        
        client server model 




2. What are the different parts of an HTTP request?


        request line
        headers
        whitespace


​
​
3. Which part of an HTTP request is optional?
​
​

        body


4. What are the three parts of an HTTP response?


    status line
    headers
    response body 


​
​
5. Which number class of status codes represents errors?


        400's and 500's error codes mean their is error on either the client side or the server side. 


​
​
6. What are the two most common request methods that a security professional will encounter?


        GET and POST




        


​
​
7. Which type of HTTP request method is used for sending data?


        POST and PUT 


​
​
8. Which part of an HTTP request contains the data being sent to the server?



        Body 
​
​
9. In which part of an HTTP response does the browser receive the web code to generate and style a web page?


Body 
​
## Using Curl
​
Answer the following questions about curl:
​
​


10. What are the advantages of using curl over the browser?
​
​       
        
        Curl can transfer data to or from a server witout user interaction. 

11. Which curl option is used to change the request method?


curl -X


​
​
12. Which curl option is used to set request headers?
​
​


        curl -H
13. Which curl option is used to view the response header?


        curl -I


​
​
14. Which request method might an attacker use to figure out which HTTP requests an HTTP server will accept?


        OPTION


​
## Sessions and Cookies
​
Recall that HTTP servers need to be able to recognize clients from one another. They do this through sessions and cookies.
​
Answer the following questions about sessions and cookies:
​
​

15. Which response header sends a cookie to the client?
​

        HTTP/1.1 200 OK
        Content-type: text/html
#     Set-Cookie: cart=Bob
​

​
​

16. Which request header will continue the client's session?
​

##        GET /cart HTTP/1.1
        Host: www.example.org
        Cookie: cart=Bob
​
## Example HTTP Requests and Responses
​
Look through the following example HTTP request and response and answer the following questions:
​
## HTTP Request
​
        POST /login.php HTTP/1.1
        Host: example.com
        Accept-Encoding: gzip, deflate, br
        Connection: keep-alive
        Content-Type: application/x-www-form-urlencoded
        Content-Length: 34
        Upgrade-Insecure-Requests: 1
        User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Mobile Safari/537.36
​
        username=Barbara&password=password
​



17. What is the request method?


        POST


​
​
18. Which header expresses the client's preference for an encrypted response?


         Upgrade-Insecure-Requests: 1


​
​



19. Does the request have a user session associated with it?



        Connection: keep-alive


​
​
20. What kind of data is being sent from this request body?


         username=Barbara&password=password


​
## HTTP Response
​
        HTTP/1.1 200 OK
        Date: Mon, 16 Mar 2020 17:05:43 GMT
        Last-Modified: Sat, 01 Feb 2020 00:00:00 GMT
        Content-Encoding: gzip
        Expires: Fri, 01 May 2020 00:00:00 GMT
        Server: Apache
        Set-Cookie: SessionID=5
        Content-Type: text/html; charset=UTF-8
        Strict-Transport-Security: max-age=31536000; includeSubDomains
        X-Content-Type: NoSniff
        X-Frame-Options: DENY
        X-XSS-Protection: 1; mode=block
​
        [page content]
​


21. What is the response status code?
​
​

        200


22. What web server is handling this HTTP response?


        Apache


​
​
23. Does this response have a user session associated to it?


        Set-Cookie: SessionID=5


​
​
24. What kind of content is likely to be in the [page content] response body?
​
​

        gzipped file 


25. If your class covered security headers, what security request headers have been included?


        X-Content-Type: NoSniff
        X-Frame-Options: DENY
        X-XSS-Protection: 1; mode=block


​
## Monoliths and Microservices
​
Answer the following questions about monoliths and microservices:
​



​
26. What are the individual components of microservices called?
​

        loadbalancer
        authentication server
        user server
        store application server
        app database
        credentials database
        Inventory database



​
27. What is a service that writes to a database and communicates to other services?



        API
​
​


28. What type of underlying technology allows for microservices to become scalable and have redundancy?
​

        Containers



​
## Deploying and Testing a Container Set
​
Answer the following questions about multi-container deployment:
​
​

29. What tool can be used to deploy multiple containers at once?
​

        Docker


​
30. What kind of file format is required for us to deploy a container set?


        yaml file 


        
## Databases
​

31. Which type of SQL query would we use to see all of the information within a table called customers?
​
​
        
        SELECT



32. Which type of SQL query would we use to enter new data into a table? (You don't need a full query, just the first part of the statement.)



        INSERT INTO

​
​

33. Why would we never run DELETE FROM <table-name>; by itself?
​


        It will delete the entire database


---
​

