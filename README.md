# ☕ Maven Basic Project 

---

# 📦 Install Maven & Java

## 🪟 Windows (Chocolatey)

```powershell
choco install maven
choco install openjdk
```

---

# ✅ Verify Installation

```bash
java --version
mvn -v
```

---

# 🚀 Create Maven Project

## 🍎 macOS / Linux

```bash
mvn archetype:generate \
-DgroupId=com.cloudnautic \
-DartifactId=maven-basic-project \
-DarchetypeArtifactId=maven-archetype-quickstart \
-DinteractiveMode=false
```

---

## 🪟 Windows PowerShell

```powershell
mvn archetype:generate `
"-DgroupId=com.cloudnautic" `
"-DartifactId=maven-basic-project" `
"-DarchetypeArtifactId=maven-archetype-quickstart" `
"-DinteractiveMode=false"
```

---

## 🪟 Windows PowerShell (With Archetype GroupId)

```powershell
mvn archetype:generate `
"-DarchetypeGroupId=org.apache.maven.archetypes" `
"-DarchetypeArtifactId=maven-archetype-quickstart" `
"-DgroupId=com.cloudnautic" `
"-DartifactId=maven-basic-project" `
"-DinteractiveMode=false"
```

---

# 📂 Navigate to Project

```bash
cd maven-basic-project
```

## 🪟 Windows

```powershell
cd \maven-basic-project
```

---

# ⚙️ Compile Project

```bash
mvn compile
```

---

# 📦 Package Project

```bash
mvn package
```

---

# ▶️ Run Java Application

## 🍎 macOS / Linux

```bash
mvn exec:java -Dexec.mainClass="com.cloudnautic.App"
```

---

## 🪟 Windows

```powershell
java -cp target\classes com.cloudnautic.App
```

---

# 📁 Important Maven Commands

| Command       | Description                               |
| ------------- | ----------------------------------------- |
| `mvn compile` | Compile source code                       |
| `mvn package` | Create JAR package                        |
| `mvn clean`   | Remove target directory                   |
| `mvn test`    | Run test cases                            |
| `mvn install` | Install package to local Maven repository |

---

# 📌 Project Structure

```text
maven-basic-project/
│
├── pom.xml
├── src/
│   ├── main/java/com/cloudnautic/App.java
│   └── test/java/com/cloudnautic/AppTest.java
└── target/
```

---

# 📌 Notes

* `pom.xml` is the Maven project configuration file.
* Source code is stored inside:

```text
src/main/java
```

* Compiled `.class` files are generated inside:

```text
target/classes
```

* Packaged `.jar` files are generated inside:

```text
target/
```
# Maven Pipeline Setup Guide

## 1. Fork the Repository

Fork the repository from GitHub:

[maven-basic-project Repository](https://github.com/atulkamble/maven-basic-project?utm_source=chatgpt.com)

* Click the **Fork** button in the top-right corner.
* This creates a copy of the repository under your GitHub account.

---

## 2. Clone the Repository

Clone the repository to your local machine:

```bash id="9t7m2q"
git clone https://github.com/atulkamble/maven-basic-project.git
```

---

## 3. Navigate to Project Directory

```bash id="2k8vjh"
cd maven-basic-project
```

---

## 4. Open Project in VS Code

```bash id="m4xg7r"
code .
```

> Make sure Visual Studio Code is installed and the `code` command is enabled.

---

## 5. Configure Git Credentials in Jenkins

### Steps

1. Open Jenkins Dashboard.
2. Navigate to:

```text
Manage Jenkins → Credentials
```

3. Add GitHub Credentials:

   * Username
   * Password / Personal Access Token (PAT)

4. Save the credentials.

> Jenkins uses these credentials to pull code from GitHub repositories.

---

## 6. Update Java Version in `pom.xml`

Open the `pom.xml` file and update the Java version properties.

### Example

```xml id="w5h9pc"
<properties>
    <maven.compiler.source>17</maven.compiler.source>
    <maven.compiler.target>17</maven.compiler.target>
</properties>
```

> Update the version number based on your project requirement.

---

## 7. Configure Jenkins Build Trigger

To automatically trigger the Jenkins job every minute, add the following cron schedule in the pipeline configuration:

```text id="1u2p9e"
* * * * *
```

### Steps

1. Open Jenkins Job.

2. Click **Configure**.

3. Go to **Build Triggers**.

4. Enable:

   * **Build periodically**

5. Add the cron expression:

```text id="z7c8lm"
* * * * *
```

> This trigger runs the Jenkins job every minute.

---

# Final Checklist

* [x] Repository forked
* [x] Repository cloned locally
* [x] Project opened in VS Code
* [x] Jenkins Git credentials configured
* [x] Java version updated in `pom.xml`
* [x] Jenkins build trigger configured (`* * * * *`)
