pipeline {
    agent {
        label 'slave'
    } 
    
    stages {
        stage('scm download') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/elurisri/python-repo.git']])
                sh 'ls'
            }
        }
        stage('test') {
            steps {
                sh 'pytest test.py'
            }
        }
        stage('buid') {
            steps {
                sh 'pytest build.py'
            }
        }
        
    }
}
