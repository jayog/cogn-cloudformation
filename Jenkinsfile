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
                withCredentials([[$class: 'UsernamePasswordMultiBinding', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
            sh "aws cloudformation create-stack --stack-name ec2-single-instance --template-body file://ec2-sg-eip-01.yaml --region 'eu-west-1'"
                }
              }
             }
            }
            }
