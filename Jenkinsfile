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
                sh 'docker build -t myubuntu .'
            }
        }  
    }
}
