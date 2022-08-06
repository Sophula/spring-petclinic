pipeline {
    agent any
    stages {
        stage('Checkout Source') {
            steps {
                checkout scm
            }
        } 
        stage('Build Application') { 
            container('M3') {
            steps {
                echo '=== Building Petclinic Application ==='
                    sh 'mvn clean package'
            }
            }
        }
    }
}
