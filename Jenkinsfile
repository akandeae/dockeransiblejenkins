pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/akandeae/dockeransiblejenkins']])
            }
        }
        stage('BUILD') {
            steps {
                sh 'docker build . -t emilokan'
            }
        }
    }
}
