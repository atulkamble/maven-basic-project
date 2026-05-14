pipeline {
    agent any

    stages {

        stage('Checkout Source Code') {
            steps {
                echo 'Checking out source code from GitHub...'
                echo 'Branch: main'
                echo 'Repository: https://github.com/atulkamble/maven-basic-project.git'
            }
        }

        stage('Verify Java Installation') {
            steps {
                echo 'Verifying Java installation...'
                sh 'java --version'
            }
        }

        stage('Verify Maven Installation') {
            steps {
                echo 'Verifying Maven installation...'
                sh 'mvn --version'
            }
        }

        stage('Clean Project') {
            steps {
                echo 'Cleaning Maven project...'
                sh 'mvn clean'
            }
        }

        stage('Compile Source Code') {
            steps {
                echo 'Compiling source code...'
                sh 'mvn compile'
            }
        }

        stage('Run Unit Tests') {
            steps {
                echo 'Running Maven tests...'
                sh 'mvn test'
            }
        }

        stage('Package Application') {
            steps {
                echo 'Packaging application...'
                sh 'mvn package'
            }
        }

        stage('Install Artifacts') {
            steps {
                echo 'Installing artifacts to local Maven repository...'
                sh 'mvn install'
            }
        }

        stage('Execute Application') {
            steps {
                echo 'Running Java application...'
                sh 'mvn exec:java -Dexec.mainClass="com.cloudnautic.App"'
            }
        }
    }

    post {

        success {
            echo 'Maven build and execution completed successfully!'
        }

        failure {
            echo 'Build failed. Please check the Jenkins console logs.'
        }

        always {
            echo 'Pipeline execution finished.'
        }
    }
}

