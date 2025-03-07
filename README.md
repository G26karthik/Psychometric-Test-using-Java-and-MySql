# Psychometric Test Application

## Overview

This project is a **Psychometric Test Application** developed in Java, designed to assess individuals' personalities, skills, and aptitudes. The application presents a series of questions to users and evaluates their responses to generate insightful results. It integrates **JDBC with MySQL** to store user responses and test results in a database.

## Features

- **User-Friendly Interface**: Simple and intuitive console-based interaction.
- **Comprehensive Question Set**: Diverse questions covering various psychometric aspects.
- **Database Integration**: Uses **JDBC with MySQL** to store and retrieve user responses.
- **Detailed Results**: Provides users with an analysis based on their responses.
- **Modular Design**: Organized code structure following Object-Oriented Programming principles.

## Prerequisites

- **Java Development Kit (JDK) 8 or later**: Ensure JDK is installed and configured in your system's PATH.
- **MySQL Database**: Install and configure MySQL.
- **JDBC Driver**: Ensure the MySQL JDBC driver (`mysql-connector-java.jar`) is available.

## Installation

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/G26karthik/OOPS-Java-PBL.git
   cd OOPS-Java-PBL
   ```

2. **Navigate to the Project Directory**:

   ```sh
   cd PsychometricTest
   ```

3. **Set Up MySQL Database**:
   - Create a new MySQL database:
     ```sql
     CREATE DATABASE psychometric_test;
     ```
   - Use the database:
     ```sql
     USE psychometric_test;
     ```
   - Create the required table:
     ```sql
     CREATE TABLE results (
         id INT AUTO_INCREMENT PRIMARY KEY,
         user_name VARCHAR(255) NOT NULL,
         score INT NOT NULL,
         timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     ```

4. **Update Database Credentials**:
   - Modify `DatabaseConfig.java` with your MySQL username and password:
     ```java
     String url = "jdbc:mysql://localhost:3306/psychometric_test";
     String user = "your_username";
     String password = "your_password";
     ```

## Project Structure

- `src/`: Contains the source code files.
  - `Main.java`: Entry point of the application.
  - `Question.java`: Defines the Question class.
  - `Test.java`: Manages the test flow and logic.
  - `Result.java`: Handles the evaluation and display of results.
  - `DatabaseConfig.java`: Manages database connection and queries.

## How to Run

1. **Compile the Java Files**:

   ```sh
   javac -cp .:mysql-connector-java.jar src/*.java
   ```

2. **Run the Application**:

   ```sh
   java -cp .:mysql-connector-java.jar src.Main
   ```

   Alternatively, you can open the project in your preferred **IDE** (such as Eclipse, IntelliJ IDEA, or VS Code with Java extensions) and run the `Main` class.

## Usage

- **Start the Test**: Follow the on-screen instructions to begin the psychometric test.
- **Answer Questions**: Respond to each question as prompted.
- **View Results**: Upon completion, the application will display your psychometric analysis and store the results in the MySQL database.
- **Retrieve Past Results**: Query the `results` table in MySQL to review stored test results:
  ```sql
  SELECT * FROM results;
  ```

## Contributing

Contributions are welcome! To contribute:

1. **Fork the Repository**.
2. **Create a New Branch**:

   ```sh
   git checkout -b feature/YourFeatureName
   ```

3. **Commit Your Changes**:

   ```sh
   git commit -m 'Add your feature'
   ```

4. **Push to the Branch**:

   ```sh
   git push origin feature/YourFeatureName
   ```

5. **Open a Pull Request**.

## License

This project is licensed under the **MIT License**.

## Acknowledgments

Special thanks to all contributors and those who provided guidance and resources for this project.

---

For any issues or questions, please open an issue in this repository.

Happy coding! 🚀

