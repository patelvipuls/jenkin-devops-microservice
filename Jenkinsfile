//Scripted

//Declarative
pipeline {
	
	agent none
	
	stages {

		stage('Permissions') {
            steps {
                sh "sudo chown root:jenkins /run/docker.sock"
            }
		}

		stage('Build') {
		  	agent { 
				  docker { 
					  image 'maven:3.6.3' 
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

