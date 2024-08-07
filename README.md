# File Hider App

The **File Hider App** is a Java application that allows users to securely hide and manage files. It provides features for user registration, login, and OTP-based authentication.

## Features

1. **Login and Signup:**
   - Users can log in with their email address.
   - New users can sign up by providing their name and email.

2. **OTP Authentication:**
   - When logging in or signing up, users receive an OTP (One-Time Password) via email.
   - Users must enter the correct OTP to proceed.

3. **File Hiding:**
   - The app allows users to hide files securely.
   - Files are encrypted and stored in a hidden location.

## Usage

1. **Clone the Repository:**
   - git clone https://github.com/Nazeer45/File_Hider-Java-MySQL.git
  
## Set Up the Database

1. **Create a database named `File_Hider`.**
2. **Use the following SQL script to create the required tables:**

   ```sql
   CREATE TABLE users (
     id INT AUTO_INCREMENT PRIMARY KEY,
     name VARCHAR(255),
     email VARCHAR(255) UNIQUE
   );

   CREATE TABLE data (
     id INT AUTO_INCREMENT PRIMARY KEY,
     name VARCHAR(255),
     path VARCHAR(255),
     email VARCHAR(255),
     bin_data TEXT,
     FOREIGN KEY (email) REFERENCES users(email)
   );

     
3. **Compile and Run:**
- Compile the Java files:
  ```
  javac Main.java
  ```
- Run the Main class:
  ```
  java Main
  ```

4. **Follow the On-Screen Instructions:**
- Choose option 1 to log in or option 2 to sign up.
- Enter your email address.
- Check your email for the OTP.
- Enter the OTP to access the app.

## Dependencies

- Java
- MySQL (for database storage)

## Contributing

Contributions are welcome! If you find any issues or have suggestions, feel free to open an issue or submit a pull request.
