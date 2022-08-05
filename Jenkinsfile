pipeline {
    agent any
    stages {
        stage('Checkout Source') {
            steps {
                url 'https://github.com/Sophula/spring-petclinic.git'
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
