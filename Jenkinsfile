pipeline {
    agent any
    stages {
        stage('Checkout Source') {
            steps {
                checkout scm
            }
        } 
        stage('Build Application') { 
            steps {
                echo '=== Building Petclinic Application ==='
                sh 'mvn clean package' 
            }
        }
    }
}
