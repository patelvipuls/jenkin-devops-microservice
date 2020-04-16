//Scripted

//Declarative
pipeline {
	agent none
	// agent any
	stages {

		stage('Permissions') {
            steps {
                sh 'chmod 775 *'
            }
}
	
		stage('Build') {
		  	agent { docker 'maven:3.6.3' } 
			steps {
				echo "Build"
				sh 'pwd'
				sh 'mvn --version'
				
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

