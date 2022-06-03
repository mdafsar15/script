pipeline {
    agent any

    stages {

	stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/mdafsar15/script.git']]])
            }
        }
        stage('build') {
            steps {
                sh './demo.sh'
            }
        }
    }
}
