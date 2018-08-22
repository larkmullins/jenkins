pipeline {
    agent {
        label 'jenkins'
    }

    stages {
        stage('Testing') {
            agent {
                docker {
                    image 'node:8-jessie'
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
