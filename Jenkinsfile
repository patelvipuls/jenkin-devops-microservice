//Scripted

//Declarative
pipeline {
	agent { docker {
			image 'maven:3.6.3'
			args '-v /root/.m2:/root/.m2' 
			} 
		} 
	// agent any
	stages {

		stage('Permissions') {
            steps {
                sh 'chmod 775 *'
            }
		}

		stage('Build') {
		 	steps {
				echo "Build"
				sh 'mvn -B -DskipTests clean package'
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

