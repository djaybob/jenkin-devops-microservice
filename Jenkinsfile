
pipeline {
	agent any
	stages {
		stage('Build'){
			echo "Build"
		}
		stage('Test'){
			echo "Test"
		}
		stage('Integration Test'){
			echo "Integration Test"
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
