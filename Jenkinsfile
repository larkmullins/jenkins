agent {
    kubernetes {
        label 'k8s-pipeline-node'
        containerTemplate {
            name 'node'
            image 'node:8-jessie'
            ttyEnabled true
            command 'cat'
        }
    }
}

agent {
    kubernetes {
        label 'k8s-pipeline-php'
        containerTemplate {
            name 'php'
            image 'php'
            ttyEnabled true
            command 'cat'
        }
    }
}

pipeline {
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
                container('php') {
                    sh 'php -v'
                }
            }
        }
    }
}
