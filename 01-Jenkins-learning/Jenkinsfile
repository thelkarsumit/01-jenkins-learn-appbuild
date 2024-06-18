pipeline {
    agent any
 
    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                 git 'https://your-repository-url.git'
            }
        }
        
        stage('Build') {
            steps {
                // Run Maven build
                sh 'mvn clean compile'
            }
        }
 
        stage('Test') {
            steps {
                // Run Maven tests
                sh 'mvn test'
            }
        }
    }
 
    post {
        always {
            // Archive the test results
            junit '**/target/surefire-reports/*.xml'
        }
    }
    // post{
      //  always {
            // Archive the test results
           // junit '**/target/surefire-reports/*.xml'
      //  }
   // }
}