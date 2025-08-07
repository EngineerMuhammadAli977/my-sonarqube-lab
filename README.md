# My SonarQube Lab 🚀

This is a simple Java Maven project integrated with **SonarQube** for static code analysis. It includes:

- ✅ Java source code (`App.java`)
- ✅ `pom.xml` configured with `sonar-maven-plugin`
- ✅ `sonar-project.properties` for standalone scans
- ✅ `Jenkinsfile` for CI pipeline with SonarQube analysis

---

## 🔧 Requirements

- Java 11+
- Maven
- SonarQube (Running on http://localhost:9000)
- Jenkins (optional, for pipeline integration)
- Docker (optional for SonarQube setup)

---

## 📦 Project Structure

```
my-sonarqube-lab/
├── Jenkinsfile
├── pom.xml
├── sonar-project.properties
└── src/
    └── main/
        └── java/
            └── com/
                └── example/
                    └── App.java
```

---

## 🚀 How to Run Analysis (Standalone)

```bash
# Compile the code
mvn clean package

# Run SonarQube scan
mvn sonar:sonar   -Dsonar.projectKey=my-sonarqube-lab   -Dsonar.host.url=http://localhost:9000   -Dsonar.login=your_token_here
```

---

## 🔄 Jenkins Integration

This repo includes a Jenkinsfile with 3 stages:

1. **Checkout**: Pulls code from GitHub
2. **Build**: Compiles using Maven
3. **SonarQube Analysis**: Executes `mvn sonar:sonar` using Jenkins Sonar plugin

Make sure Jenkins has:
- Maven tool (`Maven 3`)
- SonarQube server configured (`SonarQube`)

---

## 📚 Useful Links

- [SonarQube Documentation](https://docs.sonarsource.com/sonarqube/latest/)
- [Jenkins Pipeline Syntax](https://www.jenkins.io/doc/book/pipeline/)

---

Created by [Muhammad Ali](https://github.com/EngineerMuhammadAli977)
