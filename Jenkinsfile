pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t demo-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8085:80 demo-app || true'
            }
        }
    }
}
