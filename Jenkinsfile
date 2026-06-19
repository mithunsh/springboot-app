pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/mithunsh/springboot-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t devops-app:v1 .'
            }
        }
    }
}
