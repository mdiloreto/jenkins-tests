pipeline {
	agent any
	stages {	
		stage('Build') {
			steps{
			echo "Build"
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
