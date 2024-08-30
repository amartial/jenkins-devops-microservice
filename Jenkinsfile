// SCRIPTED APPROCHE
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Test"
// }

pipeline {
	// agent any
	agen { docker { image 'maven:3.6.3' } }
	stages {
		stage('Build') {
			 steps {
				sh 'mvn --version'
				echo "Build"
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
			echo "Im awesome. I run always"
		}
		success {
			echo "I run when you are successful"
		}
		failure {
			echo "I run when you are fail"
		}
		// changed {
		// 	echo "I run when status change 'success to failure and vise versa'"
		// }
	}
}
