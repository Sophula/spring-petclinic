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
                withMaven(maven: 'mvn') {
                sh 'mvn -B -DskipTests clean package'
                }
            }
        }
    }
}
