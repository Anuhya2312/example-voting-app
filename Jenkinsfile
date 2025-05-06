pipeline {
    agent {label 'worker'}
    options { 
        buildDiscarder(logRotator(numToKeepStr: '15'))
        disableConcurrentBuilds()
        retry(2)
        timeout(time: 15, unit: 'MINUTES')
    }
    parameters {
        string(name: 'BRANCH', defaultValue: 'develop', description: '')
        choice(name: 'ENV', choices: ['dev', 'qa', 'uat'], description: '')
    }
    environment {
    }
    triggers {
        cron('00 */4 * * *')
        pollSCM('* * * * *')
    }
    stages{
        stage("Build and Push"){
            steps{
                sh '''
                cd vote
                docker build -t anuhya23/vote:v2 .
                '''
            }
        }
        stage("Deploy"){
            steps{
                sh "echo docker run"
            }
        }
    }
}
