# CS50_Finance_Project
This is a CS50 Final Project, Which I decided to Share.
Project Name CS50
#### Video Demo:  [https://www.youtube.com/watch?v%253DuogJL_Q7ORc]
This is the final project of CS50x.
I have used website for email where the user can enter with the url and check/send emails. The project has error handlings and it shows the corresponding error. The error
message is showed with the cat meme for better interaction with the users. Following are the use cases and walkthrough how the website should be used. First the user need to
register on the mail and log in with correct password and email.The email must include "@" to be acknowledged as an email. Otherwise the website will show that username is
not available. If the error happens the cat meme will show up with the text that the username is not availabe. If one of the bar is empty or incorrect the website will show
the error. Once user is logged in on private profile, she can send email with specific subject and textual email.If the email is already registered the webstite will not
allow dublication. The error message will show that username is not available.She can also reveive email and see the specific time when she received and sent the email. In
the end user can log out from the private profile and log in when she inteds to. The website saves the sent and received data on MYSQL relational database, therefor user will
not lose the data on the website.

The flask_Sessions is the file that helps with website link generating. Once the link is available user can comprehend the features the website offers.
The static folder has file of styles.css. The file helps with graphical challendges such as font size, fort locaiton and etc.
The Templates folder has different files for specific errr handlings or pages. The apology.html shows the cat meme for the error. The Compose.html gives ability to write the email where user wants so send the email as well as the text subject and text itself.
The email.html helps with the homepage of email
index. html has the hidden elements of homepage as well as layouts of email or passowrd
the login.html give the interface of profile once the user is successfuly registered
the regiter.html gives iterface for registration
reply.html offers visuality for reply to specific email and sender.
The app,py is the file where the main project is written.
    from cs50 import SQL
    from flask import Flask, flash, redirect, render_template, request, session
    from flask_session import Session
    from tempfile import mkdtemp
    from werkzeug.security import check_password_hash, generate_password_hash
It uses MySQL for the project.db file where the data is being stored, flask for generating the website link and session. tempfile for sepecific templates and werkzeug for security and password store means.
