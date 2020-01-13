pipeline {
    agent any 
    stages {
        stage('Checkout'){
            steps{
                // find code from git
                git 'https://github.com/java2786/jendep'
            }
        }
        
        stage('Compile'){
            steps{
                // compile code
                bat label: '', script: 'mvn clean compile'
            }
        }
        
        stage('Test') { 
            steps {
                // Test code
                bat label: '', script: 'mvn test'
            }
        }

        stage('Build') { 
            steps {
                // package code
                bat label: '', script: 'mvn clean package'
            }
        }

        stage('Deploy') { 
            steps {
                // package code
                bat label: '', script: 'mvn install'
            }
        }


    }
}
