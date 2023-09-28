pipeline {
	agent any
	// agent {docker {image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
		}
		
	stages {	
		stage('Build') {
			steps{
			sh 'mvn --version'
			sh 'docker --version'
			echo "BUILD_NUMBER - $env.BUILD_NUMBER"
			}
		}
		stage('Test') {
			steps{
			echo "Test"
			}
		}
		stage ('Integration Test') {
			steps{
			echo "Integration Test"
			}
		}
	} 
	post {
		always {
			echo "Hey! Run Always finished!"
		}
		success {
			echo "Hey! Run succesfully finished!"
		}
		failure {
			echo "Hey! Run failed!"
		}
	}
}
