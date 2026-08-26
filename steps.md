```
git clone https://github.com/atulkamble/ec2-jenkins.git
cd ec2-jenkins
terraform init 
terraform plan 
terraform apply -auto-approve

apache maven 
maven integration 
java depenedency 

mvn init 
mvn build 
mvn compile 
mvn test 
mvn run 
mvn package
mvn release 


// manual run a project 
git clone https://github.com/atulkamble/maven-basic-project.git

java --version, mvn --version
mvn clean >> mvn compile >> mvn test >> mvn package >>
mvn exec:java -Dexec.mainClass="com.cloudnautic.App"

// Java/Maven Jenkins Pipeline 
Plugins: Maven Integration, Blue Ocean
Tools: myMaven myJDK

1. fork and clone https://github.com/atulkamble/maven-basic-project
2. edit Jenkinsfile >> repo your repo name 
3. create piepline >> maven-basic-project
4. triggering * * * * * 
5. git credentials >> branch - main , Jenkisfile path - same
6. build and run
```
