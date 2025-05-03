pipeline {
    agent {label 'worker'}
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
