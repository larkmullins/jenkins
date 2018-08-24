pipeline {
    agent any

    stages {
        stage('Testing') {
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
            steps {
                container('node') {
                    sh 'npm install -g serverless'
                }
            }
        }

        stage('Deploy') {
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
            steps {
                container('php') {
                    sh 'php -v'
                }
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'Jenkinsfile', fingerprint: true
        }
    }
}
