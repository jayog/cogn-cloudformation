@Library('github.com/releaseworks/jenkinslib') _
pipeline {
    agent any
    stages {
         stage('Start') {
            steps { echo "Starting..."
                }
              }
        stage('Submit Stack') {
            steps {
                withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key2', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
            bat " aws cloudformation create-stack --stack-name ec2-single-instance --template-body file://ec2-sg-eip-01.yaml --region eu-west-1 --client-request-token 'Console-CreateStack-8c5ef0c7-7b9a-a2ce-bffa-99dfafe87a3c' "
                }
              }
             }
            }
            }
