 pipeline {
    //agent any
    agent { docker { image 'maven:3.6.3'} }
	stages {
        stage('Build') {
            steps {
                sh "sudo usermod -a -G docker jenkins"
                sh "mvn --version"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
		stage('Integration Test') {
            steps {
              	echo "Integration Test"
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
