# Hospital Management System
The Hospital Management System is a Java-based application designed to manage the operations of a hospital. It allows for the management of patients and doctors, and facilitates appointment booking. The system uses a MySQL database for data storage and retrieval.

Features
Add and view patients
Add and view doctors
Book appointments
Requirements
Java Development Kit (JDK) 8 or higher
MySQL Database
JDBC driver for MySQL
Setup Instructions
Database Setup
Install MySQL and start the MySQL server.
Create a database named hospital.
Create the required tables by running the following SQL commands:
sql
Copy code
CREATE TABLE doctors (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    specialization VARCHAR(100)
);

CREATE TABLE patients (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    address VARCHAR(255),
    phone VARCHAR(15),
    disease VARCHAR(255)
);
Java Setup
Clone or download the project repository.
Ensure that the MySQL JDBC driver is included in your project’s classpath.
Update the database connection details in the HospitalManagementSystem.java file if necessary:
java
Copy code
private static final String url = "jdbc:mysql://localhost:3306/hospital";
private static final String username = "root";
private static final String password = "your_password";
Usage
Compile the Java files:
sh
Copy code
javac -d . HospitalManagementSystem.java Patient.java Doctor.java
Run the application:
sh
Copy code
java HospitalManagementSystem.HospitalManagementSystem
Follow the on-screen menu to interact with the system:
markdown
Copy code
HOSPITAL MANAGEMENT SYSTEM
1. Add Patient
2. View Patients
3. View Doctors
4. Book Appointment
5. Exit
Enter your choice:
File Descriptions
HospitalManagementSystem.java
This is the main class of the project which initializes the system, handles the user interface, and manages the interactions between patients and doctors. It connects to the MySQL database and provides options to add patients, view patients, view doctors, and book appointments.

Patient.java
This class handles all operations related to patients. It includes methods to add a patient and view all patients. The patient's information is stored in the MySQL database.

Doctor.java
This class manages the operations related to doctors. It includes methods to view all doctors and retrieve doctor details by their ID.

Authors
[Satyam Kumar Mishra]
Acknowledgements
Java Documentation
MySQL Documentation
