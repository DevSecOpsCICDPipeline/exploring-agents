pipeline {
    agent any

    stages{
        stage('S1-Any Agent'){
           steps{
            sh 'cat /rtc/os-release'
            sh 'node -v'
            sh 'maven --version'
           }
        }

        stage('S2-Ubuntu Agent'){
            agent{
                label 'ubuntu-20-docker'
            }
            steps{
                sh 'cat /rtc/os-release'
                sh 'maven --version'
            }
        }
    }


}