## Web Application Development & Security Learning Journey
* Overview

This project documents my hands-on journey of building a simple web application using Kali Linux, Apache, PHP, and MariaDB, while also learning how web applications work internally and how common security vulnerabilities appear and are fixed.

The goal was to understand both web development fundamentals and basic web application security concepts through practical implementation.

## Technologies Used
* Linux (Kali Linux)
* Apache Web Server
* PHP (Backend)
* HTML, CSS, JavaScript (Frontend)
* MariaDB (Database)
* REST-style API (JSON responses)
## Project Journey (Step-by-Step)
1. Web Server Setup
* Installed and configured Apache on Kali Linux
* Accessed the default local server via http://localhost
2. Frontend Development
* Created a basic HTML page
* Added CSS for styling
* Used JavaScript for simple client-side interactions
3. Backend Development (PHP)
* Built dynamic web pages using PHP
* Learned how server-side scripting processes user requests
4. Database Integration
* Installed and configured MariaDB
* Created a database (webapp)
* Connected PHP application to the database
5. CRUD Web Application

Built a full CRUD system:

* Create → Add user (add.php)
* Read → List users (list.php)
* Update → Edit user (edit.php)
* Delete → Remove user (delete.php)

This helped me understand how real-world applications manage data flow between frontend, backend, and database.

6. API Development
* Created a simple REST-style API (api.php)
* Learned how JSON is used to transfer data between systems
* Understood the difference between:
* HTML (for users)
* JSON (for applications)
7. Security Testing (Initial Exploration)
* Tested GET and POST parameters
* Observed how user input affects backend behavior
* Learned how improper input handling can lead to vulnerabilities
8. Security Improvements

Improved the application using:

* Prepared statements (to prevent SQL Injection)
* Input validation
* Output sanitization using htmlspecialchars()

This introduced me to basic secure coding practices.

9. Authentication System
* Built a simple login system using PHP sessions
* Implemented basic access control
* Restricted access to protected pages
* Added logout functionality
## Key Learnings

Through this project, I learned:

* How web applications are structured (Frontend → Backend → Database)
* How data flows in a web system
* How APIs work and return JSON responses
* How CRUD operations are implemented in real systems
* How common vulnerabilities occur (SQL Injection, XSS)
* How basic security measures help mitigate risks
* How authentication and session management work

## Security Note

This project is for educational purposes only.
Some initial implementations were intentionally insecure to understand vulnerabilities, and were later improved using secure coding practices.

## Conclusion

This project helped me move from basic web concepts to understanding how full web applications function in real environments. It also provided hands-on experience in both development and security fundamentals, forming a foundation for future learning in web development and cybersecurity.

## Future Improvements
* Implement password hashing (bcrypt)
* Add user roles (admin/user)
* Improve UI design
* Add CSRF protection
* Build REST API authentication (tokens)
