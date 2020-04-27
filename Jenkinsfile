pipeline {

    agent none

	stages {
		stage('Build') {
		  	agent { 
				  docker { 
					  image 'maven:3.6.3' 
                      args '-v /var/run/docker.sock:/var/run/docker.sock'
					  reuseNode true
					  }
			}
			steps {
				echo "Build"
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