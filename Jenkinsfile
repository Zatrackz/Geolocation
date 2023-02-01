pipeline {
    
    agent any
    tools{
        maven 'M2_HOME'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
                sleep 5
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
                sleep 5
            }
        }
        stage('Deploy') {
            steps {
                sh'Deploy Step'
                sleep 10
            }
        }
        stage('Docker') {
            steps {
                echo 'Image step'
            }
        }
    }
}