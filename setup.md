# Setup Instructions for Get Blood

## Prerequisites

1. **XAMPP**: Ensure XAMPP is installed on your system. You can download it from [Apache Friends](https://www.apachefriends.org/index.html).

2. **PHPMailer**: This project uses PHPMailer for email functionality. Ensure PHPMailer is included in your project dependencies.

## Installation Steps

### 1. Install XAMPP

- **Download**: Go to [Apache Friends](https://www.apachefriends.org/index.html) and download XAMPP for your operating system.
- **Install**: Run the installer and follow the instructions to install XAMPP.
- **Start Services**: Open the XAMPP Control Panel and start the Apache and MySQL services.

### 2. Clone the Repository

- Open your terminal or command prompt.
- Run the following command to clone the repository:
  ```bash
  git clone <repository-url>
### 3. Move the Project to XAMPP Directory
- Copy the project folder into the htdocs directory of your XAMPP installation.
- Windows: C:\xampp\htdocs
- macOS: /Applications/XAMPP/htdocs
### 4. Configure the Database
- Create a Database
- Open your web browser and navigate to http://localhost/phpmyadmin.
- Click on Databases and create a new database named blood_donation.
- Import the Database Schema
- Select the newly created blood_donation database.
- Click on the Import tab and upload the SQL file provided in the database folder of the repository (if available).
### 5. Configure PHPMailer
- Install PHPMailer
- If PHPMailer is not included in the repository, you can install it using Composer:
- composer require phpmailer/phpmailer
- Set Up PHPMailer Configuration
- Open the config.php or a similar configuration file in your project.
- Update the PHPMailer settings (SMTP server, username, password) according to your email provider’s specifications.
### 6. Edit Configuration Files
- Database Connection
- Open the config.php or db_config.php file and set the database connection details:
$servername = "localhost";
$username = "root"; // Default XAMPP username
$password = ""; // Default XAMPP password (empty)
$dbname = "blood_donation"; // Your database name
### 7. Access the Application
- Open your web browser and go to http://localhost/your-project-folder to start using the application.
---
## Important Notes
Sensitive Files: PHP files containing sensitive information are not included in this repository. Ensure you secure these files and follow best practices for handling sensitive data.
Troubleshooting
Apache Server Issues: If Apache doesn’t start, check if other applications are using port 80 or 443.
Database Connection Errors: Verify your database credentials and ensure MySQL is running.
