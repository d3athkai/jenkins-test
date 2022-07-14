pipeline {

	agent any	// which node to execute

	stages {

		stage("build") {
			steps {
				echo 'building application'
			}
		}

		stage("test1") {
			bash -c "hostname"
			bash -c "whoami"
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
