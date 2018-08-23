pipeline {
    agent { label 'jenkins' }

    stages {
        stage('Testing') {
            steps {
                kubernetes.pod('nodejs').withImage('nodejs').inside {
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
