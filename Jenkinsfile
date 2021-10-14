@Library('github.com/releaseworks/jenkinslib') _
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            script{
                ls
            }
            steps {
                    withAWS(credentials:'manuel1', region: 'us-east-2') {
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
