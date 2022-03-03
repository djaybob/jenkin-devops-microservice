 pipeline {
	agent any
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome:$mavenHome/bin":$PATH"
	}
   // agent { docker { image 'node:13.8'} }
	stages {
        stage('Build') {
            steps {
				echo "mvn --version"
				echo "node --version"
				echo "Path - $PATH"
				echo "BUILD_NUMBER - $BUILD_NUMBER"
				echo "BUILD_ID - $BUILD_ID"
				echo "JOB_NAME - $JOB_NAME"
				echo "BUILD_TAG - $BUILD_TAG"
				echo "BUILD_URL - $BUILD_URL"
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
