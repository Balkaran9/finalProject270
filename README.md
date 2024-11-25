# finalProject270
healthTrack

GROUP MEMBERS: ROHIT, BALKARAN SINGH

1.Project Name: 
              Health Track
2.Explanation
Business of the Application System: Health Track is a mobile and web-based health management application that
allows users to track their daily physical activities, diet, and overall well-being. The app aims to provide a
comprehensive platform for users to monitor their health progress, set personalized goals, and receive valuable
insights and recommendations based on their health data. The system offers features such as workout tracking,
calorie intake monitoring, sleep analysis, and mood monitoring. Health Track aims to help users make informed
decisions about their health and promote a healthier lifestyle.

3.Database Structure for Identity Management:
Users - [VARCHAR (100), NOT NULL]
Id    - [Primary Key, INT, Auto increment]
FirstName – [VARCHAR (50), NOT NULL, User's first name]
LastName - [VARCHAR (50), NOT NULL, User's last name]
Email - [VARCHAR (100), NOT NULL, UNIQUE]
Password – [VARCHAR (255), NOT NULL, Hashed password for secure storage.]
RegistrationDate – [DATETIME, DEFAULT CURRENT_TIMESTAMP, Date, and time when the user registered]
IsActive – [BOOLEAN, DEFAULT TRUE, indicates whether the user's account is active]
LastLogin - [ DATETIME, NULL, Timestamp of the user's last login]


4. CRUD Screens for Identity Management:

Read (Login Screen):
•	Input fields: Email and Password
•	Functionality: Validate user credentials and authenticate the user
•	Error handling: Display appropriate error messages for invalid credentials, account deactivation, or
password reset.

<form method="post" action="/login">
    <div>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    <div>
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>
    </div>
    <button type="submit">Login</button>
    <div id="error-message"></div>
</form>

Create (Create New Users Screen - Self-Registration):

•	Input fields: First Name, Last Name, Email, Password, Confirm Password
•	Functionality: Create a new user account and send a verification email to the provided email address
•	Error handling: Display appropriate error messages for invalid input, email duplication, or password mismatch.

<form method="post" action="/register">
    <div>
        <label for="firstName">First Name:</label>
        <input type="text" id="firstName" name="firstName" required>
    </div>
    <div>
        <label for="lastName">Last Name:</label>
        <input type="text" id="lastName" name="lastName" required>
    </div>
    <div>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    <div>
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>
    </div>
    <div>
        <label for="confirmPassword">Confirm Password:</label>
        <input type="password" id="confirmPassword" name="confirmPassword" required>
    </div>
    <button type="submit">Register</button>
    <div id="error-message"></div>
</form>

Update (Forgot Password Screen):

•	Input fields: Email
•	Functionality: Validate the user's email address and send a password reset link
•	Error handling: Display appropriate error messages for invalid input or email.

<form method="post" action="/forgot-password">
    <div>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    <button type="submit">Submit</button>
    <div id="error-message"></div>
</form>

Delete (Deactivate User Account Screen):

•	Input fields: Email, Password
•	Functionality: Authenticate the user and deactivate their account
•	Error handling: Display appropriate error messages for invalid input or account deactivation.

<form method="post" action="/deactivate-account">
    <div>
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    <div>
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>
    </div>
    <button type="submit">Deactivate Account</button>
    <div id="error-message"></div>
</form>

