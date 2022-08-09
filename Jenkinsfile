pipeline {
    agent {
        kubernetes {
            label 'kaniko-build-pod'
            defaultContainer 'maven'
            yamlFile 'builder.yaml'
            idleMinutes 120
        }
    }
    /*tools {
    maven 'M3'
    }*/
    stages {
        stage('Checkout Source') {
            steps {
                checkout scm
            }
        } 
        stage('maven version') {
            steps {
                sh 'mvn --version'
            }
        } 
       /* stage('Build Application') {
            steps {
                echo '=== Building Petclinic Application ==='
                sh 'mvn -B -DskipTests clean package'
            }
        }
        
        stage('Test Application') {
            steps {
                echo '=== Testing Petclinic Application ==='
                sh 'mvn test'
            }
         }
         */
        stage('Kaniko Build & Push Image') {
            steps {
              container('kaniko') {
                  sh '''
                  ls /kaniko/.docker/config.json
                  '''
             }
            }
        }
        /*stage('Deploy App to Kubernetes') {     
            steps {
              container('kubectl') {
                withCredentials([file(credentialsId: 'kubeconfig', variable: 'KUBECONFIG')]) {
                  sh 'sed -i "s/<TAG>/${BUILD_NUMBER}/" web.yaml'
                  sh 'kubectl apply -f web.yaml'
                }
              }
            }
        }*/
    }
}
