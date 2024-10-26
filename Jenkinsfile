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
                    sh 'mvn -B -DskipTests clean package'
                }
            }
        }
    }
}
