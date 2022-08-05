pipeline {
    agent any
    stages {
        stage('Build Application') { 
            steps {
                echo '=== Building Petclinic Application ==='
                sh 'mvn clean package' 
            }
        }
    }
}
