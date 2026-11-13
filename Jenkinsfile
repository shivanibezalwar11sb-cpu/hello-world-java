pipeline {
    agent any
   
    stages {
        
       stage('Compile') {
            steps {
                sh 'javac HelloWorld.java'
            }
        }
        stage('Run') {
            steps {
                sh 'java HelloWorld'
            }
        }
        stage('Package') {
            steps {
                sh 'jar cfe HelloWorld.jar HelloWorld HelloWorld.class'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'HelloWorld.jar'
            }
        }
    }
}
