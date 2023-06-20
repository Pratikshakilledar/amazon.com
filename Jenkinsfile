pipeline {
    options {
        buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
    }
    agent any

    stages {
        stage('Code Compilation') {
            steps {
                echo 'Code compilation is starting'
                sh 'mvn clean compile'
                echo 'Code compilation is completed'
            }
        }

        stage('Code Package') {
            steps {
                echo 'Code packaging is starting'
                sh 'mvn clean package'
                echo 'Code packaging is completed'
            }
        }
    }
}
