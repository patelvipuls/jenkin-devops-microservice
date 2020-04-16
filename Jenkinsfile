//Scripted

//Declarative
pipeline {
	# agent { docker { image 'maven:3.6.3'} }
	agent any
	stages {
		stage('Permissions') {
			steps {
				sh 'chmod 755 *'
			}
		}
		
		stage('Build') {
		
			steps {
				sh 'pwd'
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
			echo 'Im awesome. I run always'
		}
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run wehn you fail'
		}
	}
}

