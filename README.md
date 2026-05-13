```
choco install maven 
choco install openjdk

java --version 
mvn -v

// on mac

mvn archetype:generate \
-DgroupId=com.cloudnautic \
-DartifactId=maven-basic-project \
-DarchetypeArtifactId=maven-archetype-quickstart \
-DinteractiveMode=false

// on windows 

mvn archetype:generate `
"-DgroupId=com.cloudnautic" `
"-DartifactId=maven-basic-project" `
"-DarchetypeArtifactId=maven-archetype-quickstart" `
"-DinteractiveMode=false"

mvn archetype:generate `
"-DarchetypeGroupId=org.apache.maven.archetypes" `
"-DarchetypeArtifactId=maven-archetype-quickstart" `
"-DgroupId=com.cloudnautic" `
"-DartifactId=maven-basic-project" `
"-DinteractiveMode=false"

cd \maven-basic-project

mvn compile

mvn package 

// on mac
mvn exec:java -Dexec.mainClass="com.cloudnautic.App"

// on windows
java -cp target\classes com.cloudnautic.App
```
java -cp target\classes com.cloudnautic.App

