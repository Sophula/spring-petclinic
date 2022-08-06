pipeline {
    agent any
    tools {
      maven 'M3'
    }
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
        stage('Test Application') {
            steps {
                echo '=== Testing Petclinic Application ==='
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        }
    }
}
