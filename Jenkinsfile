pipeline {

    agent none

    stages {

		stage("permission") {

			agent any

			steps {
				sh "sudo chown jenkins: -R \$PWD/"
			}
		}
        
		stage('install maven') {

			agent { 
				docker {
					image 'maven:3.6.3'
				//	args '-u root:root'
					}
			}

            steps {
			        sh 'mvn --version'
            }

        }

	}
}
