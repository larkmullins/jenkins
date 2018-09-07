pipeline {
    agent { label 'jenkins-worker-01' }

    stages {        
        stage('Testing') {
            agent {
                docker {
                    image "node"
                }
            }
            steps {
                container('node') {
                    sh 'npm install -g serverless'
                }
            }
        }
    }
}
