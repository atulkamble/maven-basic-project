pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                echo 'branch: main https://github.com/atulkamble/maven-basic-project.git'
            }
        }

        stage('Maven') {
            steps {
                echo 'Building with Maven...'
                sh 'mvn clean install'
                sh 'mvn compile'
                sh 'mvn package'
                // sh 'mvn exec:java -Dexec.mainClass="com.cloudnautic.App"'
            }
        }
    }

    post {
        failure {
            echo 'Build failed. Please check the logs for details.'
        }

        success {
            echo 'Maven build succeeded!'
        }
    }
}