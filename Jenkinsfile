pipeline {
    agent     
        stage('Checkout Source') {
            steps {
                git 'https://github.com/Sophula/spring-petclinic.git'
            }
        } 
        stage('Build Application') { 
            steps {
                echo '=== Building Petclinic Application ==='
                sh 'mvn clean package' 
            }
        }
}
