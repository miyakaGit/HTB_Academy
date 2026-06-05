## Objective

Use a GET request to find the user with id = 1 by modifying the URL.

## Target URL
 ```http://154.57.164.63:30136/```

## Steps
1. Opened the target website in the browser.
2. Identified the GET parameter format:
```/index.php?id=0```
3. Changed the parameter value from 0 to 1:
```id=0 → id=1```
4. Final request used:
   ```http://154.57.164.63:30136/index.php?id=1```
5. Loaded the URL in the browser and retrieved the user data for ID 1.
   
## What I Learned
GET requests send data through the URL using ?parameter=value
Changing URL parameters changes the server response
Web applications use dynamic pages to serve different data from one endpoint
Basic understanding of how client-server communication works
## Conclusion

This exercise demonstrated how URL parameters control data retrieval in web applications using GET requests.
