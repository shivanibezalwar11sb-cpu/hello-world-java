pipeline {
    agent any
   
    stages {
        stage('Checkout SCM') {
            steps {
                git 'https://github.com/shivanibezalwar11sb-cpu/hello-world-java'
            }
        }
        
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
