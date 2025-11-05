pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/harrisonebsen/jenkins-pipeline-python-app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t python-demo-app .'
            }
        }
        stage('Run App') {
            steps {
                sh 'docker run -d -p 5000:5000 python-demo-app'
            }
        }
    }
}
