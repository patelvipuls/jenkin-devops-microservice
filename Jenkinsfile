pipeline {

    agent none

    stages {

        stage('install maven') {

			agent { 
				docker {
					image 'maven:3.6.3'
					args '-u root:root'
					}
			}

            steps {
			        sh 'mvn --version'
            }

        }

	}
}
