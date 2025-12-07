# 📚 EduCore Hub - Student Management System

**Complete Project Documentation & Setup Guide**

---

## 👥 Team Details

| Name | Roll Number |
|------|-------------|
| Akshat Tyagi | IMT2023551 |
| Chirayu Choudhary | IMT2023004 |
| Ishaan Sodhi | IMT2023090 |
| Nikunj Mahajan | IMT2023068 |
| Shivek Ranjan | IMT2023042 |
| Swayam Kotecha | IMT2023615 |

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

**Libraries & Dependencies**
- `mysql-connector-java` (8.0.27) - Database connectivity
- `javafx-swing` (16) - Extended GUI components
- `fest-swing` (1.2.1) - GUI testing framework
- `jdom` (1.0) - XML parsing for configuration
- `pdfbox` (2.0.27) - PDF report generation
- `junit-jupiter` (5.8.2) - Unit testing framework

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
│           ├── DBHandlerTest.java
│           ├── ConnectionViewTest.java
│           └── ManagementViewTest.java
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

### Running Tests

The project includes 26 comprehensive JUnit tests covering database operations, connection validation, and management functionality.

#### Prerequisites for Tests

```bash
# 1. Maven installed
mvn -version

# 2. MySQL running
# Windows: Services > MySQL80 > Start
# macOS: brew services start mysql
# Linux: sudo systemctl start mysql

# 3. Test database created
mysql -u root -p
mysql> CREATE DATABASE test_studentsdb;
mysql> EXIT;
```

#### Test Setup (2 Minutes)

**Step 1: Add JUnit Dependencies to pom.xml**

Add to the `<dependencies>` section:

```xml
<!-- JUnit 5 -->
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-api</artifactId>
    <version>5.8.2</version>
    <scope>test</scope>
</dependency>

<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-engine</artifactId>
    <version>5.8.2</version>
    <scope>test</scope>
</dependency>
```

**Step 2: Run All Tests**

```bash
cd StudentManagementSystem
mvn clean test
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
mvn test -Dtest=DBHandlerTest#testDatabaseConnectionSuccess

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

| Test Class | Tests | Coverage Area |
|-----------|-------|---------------|
| DBHandlerTest | 8 | Database connection, CRUD operations, SQL injection prevention, connection pooling |
| ConnectionViewTest | 8 | Connection parameter validation, MySQL connection establishment, credential validation |
| ManagementViewTest | 10 | Student CRUD operations, email/phone validation, search functionality, data display |
| **TOTAL** | **26** | **>80% Code Coverage** |

### Expected Test Results

When you run `mvn clean test`, you should see:

```
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running sms.sms.DBHandlerTest
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0 ✅

[INFO] Running sms.sms.ConnectionViewTest
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0 ✅

[INFO] Running sms.sms.ManagementViewTest
[INFO] Tests run: 10, Failures: 0, Errors: 0, Skipped: 0 ✅

[INFO] -------------------------------------------------------
[INFO] BUILD SUCCESS ✅
[INFO] Total time: 5.146s
```

### Test Descriptions

#### DBHandlerTest.java (8 Tests)
- **testDatabaseConnectionSuccess** - Verify successful MySQL connection
- **testInvalidDatabaseCredentials** - Verify connection fails with wrong credentials
- **testDatabaseInsert** - Verify INSERT operations work correctly
- **testDatabaseQuery** - Verify SELECT queries return data
- **testDatabaseUpdate** - Verify UPDATE operations modify records
- **testDatabaseDelete** - Verify DELETE operations remove records
- **testSQLInjectionPrevention** - Verify SQL injection attacks are prevented
- **testConnectionPooling** - Verify connection pool handles multiple queries

#### ConnectionViewTest.java (8 Tests)
- **testValidConnectionParameters** - Verify valid parameters pass validation
- **testEmptyHostField** - Verify empty host is rejected
- **testEmptyUsernameField** - Verify empty username is rejected
- **testInvalidPortNumber** - Verify invalid port is rejected
- **testEstablishConnection** - Verify database connection establishment
- **testInvalidHostAddress** - Verify connection fails with invalid host
- **testConnectionStringFormat** - Verify connection string format is correct
- **testSaveConnectionCredentials** - Verify credentials are saved properly

#### ManagementViewTest.java (10 Tests)
- **testAddStudentRecord** - Verify student addition works
- **testValidateStudentEmail** - Verify valid email format passes
- **testInvalidEmailFormat** - Verify invalid email is rejected
- **testDisplayAllStudents** - Verify all students can be retrieved
- **testUpdateStudentRecord** - Verify student records can be updated
- **testDeleteStudentRecord** - Verify student deletion works
- **testValidateStudentIdFormat** - Verify valid student ID format passes
- **testSearchStudentById** - Verify student search works correctly
- **testValidatePhoneNumber** - Verify valid phone number passes
- **testInvalidPhoneNumberLength** - Verify invalid phone number is rejected

---

## 📊 Database Schema

The application uses the following MySQL tables:

```sql
-- Students table
CREATE TABLE students (
    student_id VARCHAR(20) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100),
    phone VARCHAR(10),
    enrollment_date DATE
);

-- Faculties table
CREATE TABLE faculties (
    faculty_id VARCHAR(20) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100),
    department VARCHAR(50)
);

-- Courses table
CREATE TABLE courses (
    course_id VARCHAR(20) PRIMARY KEY,
    course_name VARCHAR(100) NOT NULL,
    faculty_id VARCHAR(20),
    FOREIGN KEY (faculty_id) REFERENCES faculties(faculty_id)
);

-- Attendance table
CREATE TABLE attendance (
    attendance_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id VARCHAR(20),
    course_id VARCHAR(20),
    attendance_date DATE,
    status ENUM('Present', 'Absent'),
    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id) REFERENCES courses(course_id)
);

-- Grades table
CREATE TABLE grades (
    grade_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id VARCHAR(20),
    course_id VARCHAR(20),
    grade DECIMAL(5,2),
    assignment_name VARCHAR(100),
    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id) REFERENCES courses(course_id)
);
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
  - Create test database: `mysql -u root -p` then `CREATE DATABASE test_studentsdb;`
  - Ensure MySQL credentials in tests match your setup

---

## 🔐 Security Considerations

- **Database Passwords**: Never commit database credentials to git. Use environment variables or `.env` files
- **User Authentication**: Passwords should be hashed using bcrypt or similar before storage
- **Input Validation**: All user inputs are validated server-side to prevent SQL injection
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

## 📞 Support & Contact

For issues, questions, or feature requests:
- **GitHub Issues**: [Create an Issue](https://github.com/Mushmat/StudentManagementSystem/issues)
- **Email**: Contact the project maintainers
- **Documentation**: Refer to inline code comments and this README

---

## 📄 License

This project is provided for educational purposes. Check LICENSE file for details.

---

## 🙏 Acknowledgements

- **[GitHub](https://github.com/)**: Version control and repository hosting
- **[MySQL](https://www.mysql.com/)**: Reliable database management system
- **[Oracle Java](https://www.oracle.com/java/)**: Java platform and tools
- **[Maven](https://maven.apache.org/)**: Build automation and dependency management
- **[Apache PDFBox](https://pdfbox.apache.org/)**: PDF generation library
- **Contributors**: Team members for their valuable effort and support

---

## 📝 Version History

| Version | Date | Changes |
|---------|------|----------|
| 0.0.1 | 2024-11-27 | Initial release with core functionality |
| 0.0.2 | 2024-12-07 | Added comprehensive testing suite (26 JUnit tests) |

---

**Last Updated**: December 2024  
**Status**: ✅ Active Development  
**Made with ❤️ by the EduCore Hub Team**
