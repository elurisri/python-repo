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
                sh 'apt−get install −y python3−pip'
                sh 'pip install pytest'
                sh 'pytest'
            }
        }
    }
}
