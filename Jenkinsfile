@Library('github.com/releaseworks/jenkinslib') _
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo 'Prueba de santiago'
            }
        }
        stage('Test') {
            steps {
                    withAWS(credentials: '99cd9711-d754-42fa-9eb6-dc3da9ac26ca', region: 'us-east-2') {
                        AWS("s3 ls")
                    }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
