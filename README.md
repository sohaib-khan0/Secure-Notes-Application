# Secure Notes Application

## Overview

The **Secure Notes** application is a secure web-based note-taking application that enables users to create, manage, and store their notes securely. The application uses secure authentication, encryption, and other security measures to protect user data. 

The key features of the application include:

- **Secure Authentication**: Users can register, log in, and maintain sessions securely.
- **Encrypted Notes**: Notes are encrypted before storing them in the database to ensure confidentiality.
- **User-Specific Notes**: Each user can view and manage only their own notes.
- **User-Friendly Interface**: An easy-to-use web interface with modern styling.

---

## Features

### **1. Secure Authentication**
- Passwords are hashed using **bcrypt** to prevent plain-text password storage.
- Authentication is managed using **Flask-Login** to create secure user sessions.
  
### **2. Encrypted Notes**
- Notes are encrypted using **Fernet** symmetric encryption before storing them in the database.
- Encrypted notes are decrypted only when the user needs to view them.

### **3. User Management**
- Users can register, log in, and log out.
- Each user can only access their own notes.

### **4. Secure Code Implementation**
- The application follows secure coding practices, including input validation and output encoding.
- Secure session handling, form validation, and password hashing are implemented.

---

## Getting Started

### Prerequisites

Before you start, make sure you have the following installed on your system:

- Python 3.6 or higher
- pip (Python package manager)
- SQLite (or any other relational database of your choice)

### Installation

Follow these steps to get your development environment set up:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/sohaib-khan0/secure-notes.git
    cd secure-notes
    ```

2. **Create a Virtual Environment**:
    ```bash
    python3 -m venv venv
    ```

3. **Activate the Virtual Environment**:
    - On Windows:
      ```bash
      venv\Scripts\activate
      ```
    - On macOS/Linux:
      ```bash
      source venv/bin/activate
      ```

4. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

5. **Set Up the Database**:
    The application uses SQLite by default. Run the following command to initialize the database:
    ```bash
    python app.py
    ```

---

## Usage

1. **Start the Application**:
   ```bash
   python app.py
   ```
   This will run the Flask development server, which you can access at `http://127.0.0.1:5000/`.

2. **Register an Account**:
   - Navigate to `/register` to create a new user account.
   - Provide a username and password that meets the security requirements.

3. **Login**:
   - After registration, go to `/login` to log in with your credentials.
   - Upon successful login, you'll be redirected to the dashboard where you can add, view, and manage your notes.

4. **Create Notes**:
   - Use the "Add Note" functionality to create a new encrypted note.
   - Notes are automatically encrypted before being saved to the database.

5. **View Notes**:
   - Only encrypted notes will be stored in the database.
   - When you view your notes, they will be decrypted and displayed.

---

## Security Considerations

This project implements several security mechanisms, including:

- **Password Hashing**: Using bcrypt to hash passwords before storing them.
- **Encryption**: Using **Fernet** encryption to encrypt and decrypt notes.
- **Session Management**: Ensuring secure session handling using **Flask-Login**.
- **Input Validation**: All user inputs are validated and sanitized to prevent attacks like SQL injection and XSS.

---

## Technologies Used

- **Python 3**: The programming language used to develop the application.
- **Flask**: A lightweight web framework used for the backend.
- **Flask-SQLAlchemy**: For database management.
- **Flask-Login**: For user session management.
- **Flask-WTF**: For form handling and CSRF protection.
- **Flask-Bcrypt**: For password hashing.
- **Fernet (cryptography)**: For encrypting and decrypting user notes.
- **SQLite**: The default database used for storing user data and notes.

---

## Contributing

Contributions are welcome! If you'd like to improve this project, please fork the repository, make your changes, and create a pull request. Be sure to follow best practices for security and ensure that all contributions maintain the integrity of the application.

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- **Flask Documentation**: For providing great resources on Flask development.
- **Flask-SQLAlchemy Documentation**: For database integration in Flask apps.
- **Flask-Login Documentation**: For secure session management.
- **cryptography Documentation**: For guidance on encryption and security.

---
