pipeline {
	//agent any
	agen {docker {image 'maven:3.6.3'}}
	stages {	
		stage('Build') {
			steps{
			sh 'mvn --version'
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
