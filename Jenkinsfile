pipeline {
    agent any
   
    stages {
        stage('Checkout SCM') {
            steps {
                git 'https://github.com/shivanibezalwar11sb-cpu/hello-world-java'
            }
        }
        stage('Install') {
            steps {
                sh 'sudo apt install maven'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar'
            }
        }
    }
}
