# Robot Framework Java Automation Framework

This repository contains a Robot Framework-based UI automation framework integrated with Java and Maven. The setup leverages `robotframework-maven-plugin` for executing test cases and managing dependencies.

---

## 📋 Prerequisites

Ensure you have the following installed on your local system:

1. **Java Development Kit (JDK)**  
   - [Download OpenJDK](https://jdk.java.net/)  
   - Verify installation:
     java -version


2. **Maven**  
   - Recommended version: Maven 3.8+  
   - [Download Maven](https://maven.apache.org/download.cgi)  
   - Verify installation:
 
     mvn -version


3. **Python**  
   - Recommended version: Python 3.9+  
   - [Download Python](https://www.python.org/downloads/)  
   - Ensure `pip` is installed:

     pip --version


4. **Robot Framework CLI**  
   Install the Robot Framework CLI using `pip`:
 
   pip install robotframework
Browser Drivers
Download and set up the appropriate browser driver (e.g., ChromeDriver for Chrome):
ChromeDriver
Add the driver to your system's PATH.
⚙️ Setup Instructions
Clone the Repository
Clone the repository to your local system:

bash
Copy
Edit
git clone https://github.com/your-repo/robotjavaframework.git
cd robotjavaframework
Install Maven Dependencies
Run the following command to download and set up all project dependencies:

bash
Copy
Edit
mvn clean install
Verify Directory Structure
Ensure the directory structure is as follows:

bash
Copy
Edit
RobotJavaframework/
├── pom.xml
├── src/
│   └── test/
│       └── robotframework/
│           ├── acceptance/
│           │   └── example.robot
│           └── resources/
└── target/
Add Test Cases
Add your .robot test files under src/test/robotframework/acceptance.

🛠️ Running Tests
Run All Tests
Use Maven to execute all Robot Framework test cases:

bash
Copy
Edit
mvn robotframework:run
Run Specific Test Suites
To run a specific .robot file, modify the Maven command:

bash
Copy
Edit
mvn robotframework:run -Dincludes=src/test/robotframework/acceptance/example.robot
View Test Results
Test results are generated in the target/robotframework-reports/ directory:

lua
Copy
Edit
target/robotframework-reports/
├── log.html
├── output.xml
└── report.html
Open log.html or report.html in a browser to view the results.

🐞 Troubleshooting
Error: tools.jar Not Found

Ensure you have removed all references to tools.jar from your pom.xml , If ypur using JDK > = 9 , 
Or use JDK 8 or less .

This dependency is not required in modern JDKs.
Tests Fail Due to Missing Browser Driver

Verify the appropriate browser driver (e.g., ChromeDriver) is installed and added to your system PATH.
Update the browser driver version to match your browser version.
Dependencies Fail to Download

Ensure you have a stable internet connection.
If you're behind a corporate proxy, configure Maven with proxy settings in ~/.m2/settings.xml.
📂 Project Structure
RobotJavaframework/
├── pom.xml                        # Maven configuration file
├── src/
│   ├── test/
│   │   ├── robotframework/
│   │   │   ├── acceptance/        # Robot Framework test cases
│   │   │   └── resources/         # Shared resources (e.g., variables, keywords)
│   └── main/                      # (Optional) Add Java code here for custom libraries
└── target/                        # Generated test results and compiled output
🚀 Future Enhancements
Add CI/CD integration (e.g., GitHub Actions, Jenkins) for automated test execution.
Enhance the framework with reusable custom keywords.
Expand browser support by configuring Selenium and browser drivers.
✨ Contributions
Feel free to submit issues, feature requests, or pull requests to improve the framework!

📄 License
This project is licensed under the MIT License.

💬 Contact
For questions or support, reach out to:
 Sampath K V
Email: kvsampathvg@gmail.com
