Wrote APIs to perform operations on the table `user` containing the following columns,

User Table-

Column Type
username TEXT
name TEXT
password TEXT
gender TEXT
location TEXT

---

API-1
Path: /register
Method: POST

-->If the username already exists
Status code-400
Status text-User already exists

-->If the registrant provides a password with less than 5 characters
Status code-400
Status text-Password is too short

-->Successful registration of the registrant
Status code-200
Status text-User created successfully

---

API-2
Path: /login
Method: POST

-->If an unregistered user tries to login
Status code-400
Status text-Invalid user

-->If the user provides incorrect password
Status code-400
Status text-Invalid password

-->Successful login of the user
Status code-200
Status text-Login success!

---

API-3
Path: /change-password
Method: PUT

-->If the user provides incorrect current password
Status code-400
Status text-Invalid current password

-->If the user provides new password with less than 5 characters
Status code-400
Status text-Password is too short

-->Successful password update
Status code-200
Status text-Password updated
