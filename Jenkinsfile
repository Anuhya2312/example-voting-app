pipeline {
    agent {label 'worker'}
    stages{
        stage("Build and Push"){
            steps{
                sh "cd vote"
                sh "docker build -t anuhya23/vote:v1"
            }
        }
        stage("Deploy"){
            steps{
                sh "echo docker run"
            }
        }
    }
}
