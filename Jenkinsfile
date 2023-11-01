pipeline {
    agent any 
    stages {
        stage('Compile and clean') { 
            steps {
                sh "printenv"
                sh "mvn clean compile" 
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package"
            }
        }
    }
}
