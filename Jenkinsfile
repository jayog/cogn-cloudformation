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
                withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'aws-key3', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
            bat " aws cloudformation update-stack --stack-name ec2-single-instance --template-body file://ec2-sg-eip-01.yaml --region eu-west-1 "
                }
              }
             }
            }
            }
