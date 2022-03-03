 pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                parallel(
                        "step 1": { echo "Build" },
                )
            }
        }
        stage('Test') {
            steps {
                parallel(
                        "step 1": { echo "Test" },
                )
            }
        }
		stage('Integration Test') {
            steps {
                parallel(
                        "step 1": { echo "Integration Test" },
                )
            }
        }
    }
	post {
		always {
			echo "always"
		}
		success {
			echo "success"
		}
		failure {
			echo "failure"
		}
	}
}