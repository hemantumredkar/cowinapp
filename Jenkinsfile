pipeline {
    options {
        buildDisorder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
    }

    agent any

    tools {
        maven 'maven_3.8.1'
    }

    stages {
        stage ('Code Compilation') {
            steps {
                echo 'code compilation is in progress'
                sh 'mvn --version'
                sh 'mvn clean package'
            }
        }

        stage ('Code QA Execution') {
            steps {
                echo 'Junit test case check in progress'
                sh 'mvn --version'

            }
        }

        stage ('Code package') {
            steps {
                echo 'Creating war file'
                sh 'mvn clean package'
            }
        }
    }
}