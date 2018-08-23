pipeline {
    agent {
        kubernetes {
            label 'jenkins-worker'
            containerTemplate {
                name 'node'
                image 'node:8-jessie'
                ttyEnabled true
                command 'cat'
            }
        }
    }

    stages {
        stage('Testing') {
            steps {
                container('node') {
                    sh 'npm install -g serverless'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy"
            }
        }
    }
}
