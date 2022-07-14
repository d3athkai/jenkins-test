pipeline {

	agent any	// which node to execute

	stages {

		stage("build") {
			when {
				changeset pattern: "Jenkinsfile"
			}
			steps {
				echo 'building application'
			}
		}

		stage("deploy") {
			steps {
				echo 'deploying application'
			}
		}

	}

	post {
		always {
			// always executed
			echo "always"
		}
		success {
			// executed only when success
			echo "success"
		}
		failure {
			// executed only when failed
			echo "failure"
		}
	}
}
