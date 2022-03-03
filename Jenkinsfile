 pipeline {
    //agent any
    agent { docker { image 'maven:3.6.3'} }
	stages {
        stage('Build') {
            steps {
                sh "mvn --version"
            }
        }
        stage('Test') {
            steps {
                "step 1": { echo "Test" }
            }
        }
		stage('Integration Test') {
            steps {
              	"step 1": { echo "Integration Test" }
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