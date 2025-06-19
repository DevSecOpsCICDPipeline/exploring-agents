pipeline {
    agent any

    stages{
        stage('S1-Any Agent'){
           steps{
            sh 'cat /ect/os-release'
            sh 'node -v'
            sh 'mvn --version'
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
    }


}