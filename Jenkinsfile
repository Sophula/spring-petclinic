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
                def mvnHome = tool name: 'Apache Maven 3.8.6', type: 'maven'
                sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
            }
        }
    }
}
