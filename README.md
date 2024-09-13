# **CS50 Finance Project**

*This is my final project for CS50x, which I decided to share with the community.*

### **Video Demo**: [CS50 Final Project Demo](https://www.youtube.com/watch?v%253DuogJL_Q7ORc)

---

## **Project Overview**
This project is a web-based email system where users can register, log in, send, and receive emails. The website includes error handling, session management, and database integration. Error messages are displayed in a fun and interactive way using cat memes.

---

## **Key Features**:
*1. User Registration & Authentication:*
   - Users can register with a valid email address (must include "@" symbol).
   - A password is required, and the user must log in with their correct credentials.
   - If a user tries to register with an already registered email or invalid credentials, an error message with a cat meme will appear.

*2. Email Management:*
   - Once logged in, users can compose and send emails by specifying a subject and email body.
   - Duplicate emails (same address) are not allowed, and an error will be shown.
   - Users can receive emails, view messages, and see the time and date of sent or received emails.

*3. Session Management:*
   - Users can log in to their private profiles and stay logged in throughout the session.
   - After finishing, they can log out and return at any time.
   - Sessions ensure secure and personalized user experiences.

*4. Error Handling:*
   - The site provides various error messages for invalid inputs like missing fields, incorrect credentials, or duplicate registrations.
   - Cat memes are used to display errors for better user interaction.

*5. Database Management:*
   - The project uses MySQL (`project.db`) to store user data, emails, and other information.
   - Data is persistent, so users do not lose their emails or details when returning.

---

## **Walkthrough**:

*1. Registration:*  
   - Navigate to the registration page.  
   - Provide a valid email and password.  
   - If successful, the user is redirected to their private profile.  
   - Errors like missing fields or an invalid email format will trigger a cat meme error message.

*2. Logging In:*  
   - Use the registered email and password to log in.  
   - If credentials are invalid, an error message will appear.

*3. Sending Emails:*  
   - After logging in, users can compose a new email with a subject and body.  
   - If the email address is already in the system, duplicate emails are not allowed.

*4. Receiving Emails:*  
   - Users can view incoming emails, check the timestamp, and reply.

*5. Logging Out:*  
   - Users can log out from their profile after use.  
   - The session will securely end, and users can log back in when needed.

---

## **File Structure**:

- `flask_Sessions.py`:  
   *Handles session management and URL generation for the website.*

- `static/styles.css`:  
   *Handles the graphical aspects of the website, such as fonts and layouts.*

- `templates/`:  
   *Contains various HTML files for different pages and error handling, including:*
   - `apology.html`: Displays cat meme error messages.
   - `compose.html`: Allows users to compose new emails.
   - `email.html`: Displays the homepage for email functionality.
   - `index.html`: Contains the hidden elements for email layout.
   - `login.html`: Interface for user login.
   - `register.html`: Interface for new user registration.
   - `reply.html`: Visual interface for replying to emails.

- `app.py`:  
   *Main file that contains the project logic. Uses Flask for web framework, MySQL for data storage, and various libraries like Werkzeug for security.*

---

## **Technologies Used**:

- **Flask**: Web framework for handling routes and rendering pages.
- **MySQL**: Relational database for storing user and email data.
- **Flask Session**: For managing user sessions.
- **Werkzeug**: Security library for password hashing.
