pipeline {

    agent none

    stages {

		stage('install maven') {

			agent { 
				docker {
					image 'maven:3.6.3'
				//	args '-u root -p 8081:8081 -v /var/run/docker.sock:/var/run/docker.sock  '
					}
			}

            steps {
			        sh 'mvn --version'
            }

        }

	}
}