pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'b301b6a8-0aaf-44fd-b291-5d2b99797dd3', url: 'https://github.com/benbobyabraham/testjenkins']])
            }
        }
        stage('Build'){
            steps{
                git branch: 'main', credentialsId: 'b301b6a8-0aaf-44fd-b291-5d2b99797dd3', url: 'https://github.com/benbobyabraham/testjenkins'
                sh 'python3 list_python.py'
            }
        }
        stage('Test'){
            steps{
                echo "The job has been tested"
            }
        }
    }
}
