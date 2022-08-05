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
                withMaven(maven: 'maven_3_8_6') {
                    sh 'mvn -B -DskipTests clean package'
                }
            }
        }
    }
}
