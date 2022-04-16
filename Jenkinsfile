//DECLARATIVE 
pipeline {
	agent any
	environment {
		mavenHome = tool 'myMaven'
		PATH = "$PATH:$mavenHome/bin"
	}
	stages {
		stage('Compile'){
			steps {
				echo "mvn --version"
				echo "mavenHome - $mavenHome"
				echo "PATH - $PATH"
				
				sh "mvn clean compile"
			}
		}
		stage('Test'){
			steps {
				sh "mvn test"
			}
		}
		stage('Integration Test'){
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
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
