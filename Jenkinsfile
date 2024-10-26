pipeline {
    agent any
    options {
       timestamps()
       timeout(time: 1, unit: 'HOURS')
    }
    environment {
        ECR_PRIVATE_REGISTRY_URL = "590184116223.dkr.ecr.eu-west-3.amazonaws.com"
        AWS_ACCOUNT_ID="590184116223"
        AWS_DEFAULT_REGION="eu-west-3"
    }
    parameters {
        booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Toggle this option to deploy')
    }
    stages {
        stage('Build') {
            steps {
                script {
                    // Build the application using Maven
                    sh 'mvn clean package'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests
                    sh 'mvn test'
                }
            }
        }
        stage('Docker Build') {
            steps {
                script {
                    // Run Docker build in order to build image
                    //h ''
                }
            }
        }
        stage('Docker Push') {
            steps {
                script {
                    // Run Docker push in order to push image into a Registry
                    //sh ''
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Deploy the application (customize as needed)
                    // This could involve copying files, starting services, etc.
                    echo 'Deploying application...'
                }
            }
        }
    }
}
