pipeline {
    agent any

    stages{
        stage('S1-Any Agent'){
           steps{
            sh 'cat /etc/os-release'
            // sh 'mvn --version'
           }
        }

        stage('S2-Ubuntu Agent'){
            agent{
                label 'ubuntu-docker-jdk17-node20'
            }
            steps{
                sh 'cat /etc/os-release'
                sh 'mvn --version'
            }
        }

        stage('S3-Docker Image Agent'){
           agent {
                docker {
                alwaysPull true
                image 'node:18-alpine'
                // label 'ubuntu-docker-jdk17-node20'
                }
          }
          steps{
             sh 'cat /etc/os-release'
             sh 'node -v'
             sh 'npm  -v'
          }

        }
    }


}