# 📚 EduCore Hub - Student Management System

**Complete Project Documentation & Setup Guide**

---

## 👥 Team Details

| Name | Roll Number |
|------|-------------|
| Shivek Ranjan | IMT2023042 |
| Navish | IMT2023060 |
| Digvijaysinh Pawar | IMT2023099 |

---

## 📖 Project Overview

**EduCore Hub** is a comprehensive Java Swing-based desktop application designed to streamline the management and handling of student and faculty data. The system enables administrators and faculty members to efficiently manage student records, attendance tracking, grade assignments, and generate performance reports.

### Mission

To provide an efficient, user-friendly solution that simplifies the administrative tasks involved in managing student information, enabling educators and administrators to focus on supporting student success.

---

## 🎯 Project Objectives

- **Facilitate student data management**: Enable administrators to add, update, and delete student records with ease
- **Streamline attendance tracking**: Provide faculty with a simple interface to mark student attendance accurately
- **Enhance grading transparency**: Automate the grading process to ensure accurate evaluation
- **Support course and faculty association**: Allow faculties to manage courses and assign students dynamically
- **Simplify user authentication**: Implement secure login systems for authorized access
- **Provide comprehensive reporting**: Generate detailed student progress reports

---

## ✨ Key Features

### Core Functionality
- ✅ **Student Record Management** - Add, edit, and delete student data with validation
- ✅ **Attendance Tracking** - Mark and review attendance with date validation
- ✅ **Grading Automation** - Assign and update grades through integrated C++ processors
- ✅ **Faculty Course Selection** - Link faculties with specific courses
- ✅ **Secure Login** - Separate authentication for admins and faculty members
- ✅ **Multi-Role Access** - Admin and faculty-specific dashboards with role-based permissions
- ✅ **Database Integration** - Secure data storage using MySQL
- ✅ **Error Handling** - Input validation and user-friendly error messages
- ✅ **Report Generation** - Generate and download student performance reports in PDF format
- ✅ **Date Validation** - Support for structured date formats (YYYY-MM-DD)

---

## 🏗️ Technical Architecture

### Technology Stack

**Frontend**
- Framework: **Java Swing** for GUI development
- UI Components: JTable, JComboBox, JTextField, JButton, JDialog
- Styling: Cross-platform Java Swing theming

**Backend**
- Language: **Java** (JDK 11+) for core business logic and database operations
- Database: **MySQL 8.0+** for storing student, course, faculty, and attendance data
- Integration: **C++ executables** for attendance and grading processing logic

**Build & Deployment**
- Build Tool: **Maven 3.6+** for dependency management and project building
- Version Control: **Git** for source code management
- IDE Support: IntelliJ IDEA / Eclipse

**Testing Framework**
- **FEST Swing** (1.2.1) - GUI testing framework for testing Swing components
- **JUnit 4** - Unit testing framework for core logic testing

**Libraries & Dependencies**
- `mysql-connector-java` (8.0.27) - Database connectivity
- `javafx-swing` (16) - Extended GUI components
- `fest-swing` (1.2.1) - GUI testing framework
- `jdom` (1.0) - XML parsing for configuration
- `pdfbox` (2.0.27) - PDF report generation
- `junit` (4.13.2) - Unit testing framework

### Project Structure

```
StudentManagementSystem/
├── src/
│   ├── main/
│   │   ├── java/sms/
│   │   │   ├── DBHandler.java              # Database operations
│   │   │   ├── ConnectionView.java         # Database connection UI
│   │   │   ├── ManagementView.java         # Admin management panel
│   │   │   ├── LoginView.java              # Login interface
│   │   │   ├── FacultyLoginView.java       # Faculty login
│   │   │   ├── MainSelectionView.java      # Main menu
│   │   │   ├── FacultyHomePage.java        # Faculty dashboard
│   │   │   ├── FacultyStudentView.java     # Faculty student view
│   │   │   ├── TakeAttendanceView.java     # Attendance marking
│   │   │   ├── GradeStudentsView.java      # Grade assignment
│   │   │   ├── DownloadReportsView.java    # Report generation
│   │   │   ├── Student.java                # Student data model
│   │   │   ├── Translator.java             # Internationalization
│   │   │   └── ... (other classes)
│   │   └── resources/
│   │       └── executables/
│   │           ├── AttendanceProcessor.exe
│   │           ├── GradeProcessor.exe
│   │           └── PasswordGenerator.exe
│   └── test/
│       └── java/sms/sms/
│           ├── DBHandlerTest.java                # Database logic tests
│           ├── ConnectionViewTest.java          # Connection GUI tests
│           └── ManagementViewTest.java          # Management GUI tests
├── Languages.xml                # Configuration file
├── pom.xml                       # Maven configuration
└── README.md                     # This file
```

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Java Development Kit (JDK) 11 or higher**
  - Download: https://www.oracle.com/java/technologies/downloads/
  - Verify: `java -version`

- **MySQL Server 8.0 or higher**
  - Download: https://dev.mysql.com/downloads/mysql/
  - Note down your MySQL username and password during installation

- **Maven 3.6 or higher**
  - Download: https://maven.apache.org/download.cgi
  - Verify: `mvn -version`

- **Git** (for cloning the repository)
  - Download: https://git-scm.com/

---

## 📋 Installation & Setup

### Option 1: Quick Start (Pre-built JAR)

1. **Download the pre-built JAR file** from the [Google Drive link](https://drive.google.com/drive/folders/1nMiEeCQOFQeBRboBLAmh8gNAsqKZ2-cK?usp=sharing)

2. **Extract the downloaded files** and ensure you have:
   - `S-M-S-0.0.1-SNAPSHOT.jar`
   - `Languages.xml`
   - `AttendanceProcessor.exe`
   - `GradeProcessor.exe`
   - `PasswordGenerator.exe`

3. **Create MySQL Database**:
   ```bash
   mysql -u root -p
   ```
   Enter your password when prompted, then run:
   ```sql
   CREATE DATABASE studentsdb;
   ```

4. **Run the Application**:
   ```bash
   java -jar S-M-S-0.0.1-SNAPSHOT.jar
   ```

5. **Login Credentials**:
   - Enter your MySQL username and password when prompted
   - Use the default admin credentials (if configured)

---

### Option 2: Build from Source

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Mushmat/StudentManagementSystem.git
   cd StudentManagementSystem
   ```

2. **Install Dependencies**:
   ```bash
   mvn clean install
   ```

3. **Build the Project**:
   ```bash
   mvn clean package
   ```
   This generates a `target/` folder with the compiled JAR.

4. **Prepare Runtime Files**:
   ```bash
   cd target/
   # Copy these files into the target folder:
   # - Languages.xml
   # - AttendanceProcessor.exe
   # - GradeProcessor.exe
   # - PasswordGenerator.exe
   ```

5. **Create MySQL Database**:
   ```bash
   mysql -u root -p
   ```
   Run:
   ```sql
   CREATE DATABASE studentsdb;
   ```

6. **Run the JAR**:
   ```bash
   java -jar S-M-S-0.0.1-SNAPSHOT.jar
   ```

7. **First Launch**:
   - The application will prompt for MySQL connection details
   - Enter your MySQL username and password
   - The system will automatically create required tables
   - Login with admin/default credentials

---

## 🧪 Testing & Quality Assurance

The project includes comprehensive test suites covering both GUI and database logic using JUnit and FEST Swing frameworks.

### Running Tests

#### Prerequisites for Tests

```bash
# 1. Maven installed
mvn -version

# 2. MySQL running
# Windows: Services > MySQL80 > Start
# macOS: brew services start mysql
# Linux: sudo systemctl start mysql

# 3. Database created
mysql -u root -p
mysql> CREATE DATABASE studentsdb;
mysql> EXIT;
```

#### Test Execution Commands

```bash
# Run all tests
mvn clean test

# Run specific test class
mvn test -Dtest=DBHandlerTest
mvn test -Dtest=ConnectionViewTest
mvn test -Dtest=ManagementViewTest

# Run specific test method
mvn test -Dtest=DBHandlerTest#checkIfTableExistsTest

# Generate code coverage report
mvn clean test jacoco:report

# View coverage report (macOS)
open target/site/jacoco/index.html

# View coverage report (Linux)
xdg-open target/site/jacoco/index.html

# View coverage report (Windows)
start target/site/jacoco/index.html

# Skip tests during build
mvn clean package -DskipTests
```

### Test Coverage

| Test Class | Tests | Framework | Coverage Area |
|-----------|-------|-----------|---------------|
| **DBHandlerTest** | 3+ | JUnit 4 | Database logic, table verification, faculty/course CRUD |
| **ConnectionViewTest** | 3 | FEST Swing | Connection form validation, database connection, error handling |
| **ManagementViewTest** | 15+ | FEST Swing | GUI interactions, student CRUD, form validation, error messages |

### Test Descriptions

#### DBHandlerTest.java (Core Database Logic Tests)

Using JUnit 4 framework to test backend database operations:

- **checkIfTableExistsTest** - Verifies table existence checking with various inputs
  - Tests valid tables: students, courses, faculties
  - Tests invalid inputs: non-existent tables, special characters, empty strings
  
- **addFacultyTest** - Tests faculty addition to database
  - Normal faculty names
  - Special characters and numbers
  - Edge cases: empty strings, spaces
  
- **addCourse** - Tests course addition functionality
  - Various course durations (positive, negative, zero)
  - Faculty association validation

#### ConnectionViewTest.java (Database Connection GUI Tests)

Using FEST Swing framework to test GUI components:

- **emptyFieldsTest** - Validates error when connection fields are empty
  - Expected: "Please fill in all the empty fields!"
  
- **wrongDatabaseUrl** - Tests connection with invalid database URL
  - Expected: "Connection with the database hasn't been established! Please check your credentials!"
  
- **correctCredentials** - Tests successful database connection
  - Expected: "Connection with the database has been successfully established!"

#### ManagementViewTest.java (Student Management GUI Tests)

Comprehensive GUI testing using FEST Swing:

**Student Management Tests:**
- **emptyFieldsTest** - Validates error for empty student form fields
- **addStudentSuccessfully** - Tests successful student addition with valid data
- **addStudentWithWrongAge** - Tests validation of non-numeric age input
- **addStudentWithWrongStartedDate** - Tests date format validation (YYYY-MM-DD)
- **deleteWithoutSelection** - Tests error when deleting without selecting student

**Faculty Management Tests:**
- **addFacultySuccessfully** - Tests faculty addition workflow
- **addFacultyThatExists** - Tests duplicate prevention for faculties

**Course Management Tests:**
- **addCourseSuccessfully** - Tests course creation with valid data
- **addCourseWithoutName** - Tests error handling for missing course name
- **addCourseWithWrongDuration** - Tests duration validation (digits only)
- **addCourseThatExists** - Tests duplicate prevention for courses

**General Tests:**
- **disconnectWarning** - Tests disconnect confirmation dialog

### Expected Test Results

When you run `mvn clean test`, you should see:

```
Tests run: 21+, Failures: 0, Errors: 0, Skipped: 0
BUILD SUCCESS
```

### Running Tests Individually

```bash
# Test database operations only
mvn test -Dtest=DBHandlerTest

# Test connection GUI
mvn test -Dtest=ConnectionViewTest

# Test management GUI
mvn test -Dtest=ManagementViewTest
```

---

## 💻 Usage Guide

### For Administrators

1. **Login** with admin credentials
2. **Manage Students**:
   - Click "Add Student" to create new student records
   - Edit existing records by selecting and clicking "Edit"
   - Delete records with confirmation
3. **Manage Faculties**: Add faculty members and assign courses
4. **View Reports**: Access student performance reports

### For Faculty Members

1. **Login** with faculty credentials
2. **Mark Attendance**:
   - Select course and date
   - Check boxes for present students
   - Submit attendance
3. **Assign Grades**:
   - Select student and assignment/exam
   - Enter grade and submit
4. **Generate Reports**:
   - View student performance metrics
   - Download attendance and grade reports

---

## 🔧 Configuration

### Languages.xml

This file contains configuration for the application. Modify as needed:

```xml
<configuration>
    <database>
        <host>localhost</host>
        <port>3306</port>
        <database>studentsdb</database>
    </database>
    <ui>
        <theme>default</theme>
        <language>English</language>
    </ui>
</configuration>
```

### Maven Properties

Edit `pom.xml` to customize build settings:

```xml
<properties>
    <maven.compiler.source>11</maven.compiler.source>
    <maven.compiler.target>11</maven.compiler.target>
    <maven.compiler.release>11</maven.compiler.release>
</properties>
```

---

## 🐛 Troubleshooting

### Issue: "Cannot connect to MySQL database"
- **Solution**: 
  - Ensure MySQL server is running: `mysql.server start` (macOS/Linux) or check Services (Windows)
  - Verify username and password are correct
  - Check if database `studentsdb` exists: `SHOW DATABASES;`

### Issue: "Missing executables: AttendanceProcessor.exe not found"
- **Solution**: 
  - Copy `.exe` files to the target directory
  - Ensure they are in the same directory as the JAR file
  - Windows only: Ensure Visual C++ redistributables are installed

### Issue: "Exception in thread 'main' java.lang.ClassNotFoundException"
- **Solution**: 
  - Rebuild project: `mvn clean package`
  - Delete `target/` folder and rebuild
  - Ensure Maven dependencies are downloaded

### Issue: "OutOfMemoryError" when generating large reports
- **Solution**: 
  - Increase JVM memory: `java -Xmx2048m -jar S-M-S-0.0.1-SNAPSHOT.jar`
  - Limit report date ranges to smaller periods

### Issue: "Permission denied" on Linux/macOS
- **Solution**: 
  - Make `.exe` files executable: `chmod +x *.exe`
  - Or use Wine/Mono to run Windows executables on Unix systems

### Tests Fail: "Connection refused"
- **Solution**:
  - Start MySQL: `brew services start mysql`
  - Create database: `mysql -u root -p` then `CREATE DATABASE studentsdb;`
  - Ensure MySQL credentials in tests match your setup

### Tests Fail: "FEST Swing initialization error"
- **Solution**:
  - Ensure FEST Swing dependency is in pom.xml
  - Tests require GUI to be available (may fail in headless environments)
  - Use Xvfb on Linux to provide virtual display: `xvfb-run mvn test`

---

## 🔐 Security Considerations

- **Database Passwords**: Never commit database credentials to git. Use environment variables or `.env` files
- **User Authentication**: Passwords should be hashed using bcrypt or similar before storage
- **Input Validation**: All user inputs are validated to prevent SQL injection
- **Access Control**: Role-based access ensures faculty cannot access admin functions
- **Data Privacy**: Sensitive student data should comply with FERPA/GDPR regulations

---

## 📈 Performance Optimization

- **Database Indexing**: Indexed primary keys and foreign keys for fast queries
- **Connection Pooling**: Uses connection pooling for efficient database access
- **Lazy Loading**: Student records loaded on-demand to reduce memory usage
- **Report Caching**: Generated reports cached to avoid redundant calculations

---

## 🚀 Future Scope

- **Cloud Integration**: Transition to cloud infrastructure (AWS, Google Cloud) for greater scalability
- **AI-Powered Analytics**: Machine learning models to predict student performance and identify at-risk students
- **Mobile App**: Cross-platform mobile application for iOS and Android
- **Real-time Notifications**: SMS/Email alerts for attendance and grade updates
- **Biometric Authentication**: Fingerprint or facial recognition for secure attendance
- **Advanced Analytics Dashboard**: Interactive charts and analytics for administrators
- **API Integration**: RESTful API for third-party integrations
- **Multilingual Support**: Support for multiple languages in the UI

---

## 🙏 Acknowledgements

- **[GitHub](https://github.com/)**: Version control and repository hosting
- **[MySQL](https://www.mysql.com/)**: Reliable database management system
- **[Oracle Java](https://www.oracle.com/java/)**: Java platform and tools
- **[Maven](https://maven.apache.org/)**: Build automation and dependency management
- **[Apache PDFBox](https://pdfbox.apache.org/)**: PDF generation library
- **[FEST Swing](https://github.com/alexruiz/fest-swing)**: GUI testing framework

---

