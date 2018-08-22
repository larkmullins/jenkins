pipeline {
    agent {
        docker {
            image 'nginx'
        }
    }

    stages {
        stage('Testing') {
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
