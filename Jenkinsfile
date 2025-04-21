pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/bukharyi/practical_8_github_action.git'
            }
        }
        stage('Build') {
            steps {
                bat 'start gradlew build'
            }
        }
        stage('Test') {
            steps {
                bat 'start gradlew test'
            }
        }
        stage('Deploy') {
            steps {
                powershell 'java -jar build/libs/hello-world-java-V1.jar'
            }
        }
    }
}