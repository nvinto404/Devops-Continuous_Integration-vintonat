pipeline {
    agent any 
    stages {
        timestamps {
 stage ('Checkout') {
            steps {
                sh 'echo checkout'
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/nvinto404/Devops-Continuous_Integration-vintonat']])
            }
        }
        stage ('Test') {
            steps {
                sh 'echo test'
                junit '**/test-results/test/*.xml'
            }
        }
        stage ('Deploy') {
            steps {
                sh 'echo deploy'
            }
        }
    }
    }
}