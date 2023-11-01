pipeline {
    agent any 
    stages {
        stage('Compile and clean') { 
            steps {
                sh "rm -rf jenkins-maven"
                sh "git clone https://github.com/vaishnavi-196/jenkins-maven.git"
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
