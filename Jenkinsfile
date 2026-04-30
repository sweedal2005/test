pipeline {
    agent any

    tools {
        maven 'Mavn3'
    }

    stages {

        stage('CHECKOUT') {
            steps {
                git 'https://github.com/sweedal2005/test.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }
    }
}
