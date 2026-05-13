# ☕ Maven Basic Project Setup Guide

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
