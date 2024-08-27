pipeline {
    agent any
    environment {
        PATH = "/usr/local/bin:${env.PATH}"
    }
    stages {
        stage('Hello') {
            steps {
                sh 'echo "Executing sh command"'
                sh 'whoami'
                echo 'Hello World'
            }
        }
        stage('with docker') {
            steps {
                sh 'docker --version'
                // sh 'docker inspect -f . node:18-alpine'
            }
        }
        stage('test') {
            steps {
                sh 'echo "this is a test stage"'
                sh 'test -f src/index.js'
            }
        }
    }
}
