pipeline {
    agent any

    stages {
        stage('scm download') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/elurisri/python-repo.git']])
                sh 'ls'
            }
        }
        stage('test') {
            steps {
                sh 'sudo apt update'
                sh 'sudo apt install python3'
                sh 'python3 test.py'
                sh 'ls'
            }
        }
    }
}
