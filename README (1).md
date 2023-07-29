## Setup Instructions for Running Spring Boot Application on AWS

1. **Pull Project from GitHub:**
   - Install Git (if not already installed):
     ```
     sudo apt-get update
     sudo apt-get install git
     ```
   - Clone your Spring Boot project from GitHub:
     ```
     git clone https://github.com/your-username/your-spring-boot-project.git
     cd your-spring-boot-project
     ```

2. **Install Java:**
   - Install default JRE and OpenJDK 17 JDK:
     ```
     sudo apt-get install default-jre
     sudo apt-get install openjdk-17-jdk
     ```
   - Set JAVA_HOME environment variable:
     ```
     export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
     export PATH=$PATH:$JAVA_HOME/bin
     ```

3. **Check Java Version:**
   - Verify that the correct Java version is set:
     ```
     java -version
     ```

4. **Choose Java Version (Optional):**
   - List available Java versions (if applicable):
     ```
     sudo update-java-alternatives --list
     ```
   - Set the desired version (e.g., OpenJDK 17):
     ```
     sudo update-java-alternatives --set java-17-openjdk-amd64
     ```

5. **Remove Older Java Versions (Optional):**
   - Remove older Java versions (if needed):
     ```
     sudo apt-get purge openjdk-\*
     ```

6. **Update Package Manager and Install Maven:**
   - Update the package manager and install Maven:
     ```
     sudo apt-get update
     sudo apt-get install maven
     ```

7. **Build and Package the Spring Boot Application:**
   - Clean and install the project using Maven:
     ```
     mvn clean
     mvn install
     ```

8. **Run the Spring Boot Application:**
   - Run the Spring Boot application without detaching from the terminal:
     ```
     mvn spring-boot:run
     ```
   - OR, to run in the background with 'nohup':
     ```
     nohup mvn spring-boot:run &
     ```

9. **Run the Spring Boot Application with JAR:**
   - If you prefer running the JAR file directly:
     ```
     java -jar target/res_spring_reactive-0.0.1-SNAPSHOT.jar
     ```
   - OR, to run in the background with 'nohup':
     ```
     nohup java -jar target/res_spring_reactive-0.0.1-SNAPSHOT.jar &
     ```

Make sure to follow these steps to successfully set up and run your Spring Boot application on AWS. Adjust the instructions based on your specific project and requirements.
