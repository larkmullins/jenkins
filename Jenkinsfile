pipeline {
    agent {
        label 'jenkins-k8s'
    }

    stages {
        stage('Testing') {
            agent {
                docker {
                    image 'nginx'
                }
            }
            steps {
                echo "Testing"
            }
        }

	stage('Deploy') {
	    steps {
		echo "Deploy"
	    }
	}
    }
}
