pipeline {

    agent any

    stages {

        stage('Build') {

            steps {
				sh 'sudo docker pull maven:3.6.3'
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
