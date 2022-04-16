//DECLARATIVE 
pipeline {
	agent any
	stages {
		stage('Build'){
			steps {
				echo 'Build'
			}
		}
		stage('Test'){
			steps {
				echo 'Test'
			}
		}
		stage('Integration Test'){
			steps {
				echo 'Integration Test'
			}
		}
	}
}

post {
	always {
		echo 'always statement ran'
	}
	success {
		echo 'success statement ran'
	}
	failure {
		echo 'failure statement ran'
	}
}

//SCRIPTED 
/*
node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test') {
		echo "Integration Test"
	}
}
*/
