pipeline {

    agent none

    stages {

		stage("permission") {

			agent any

			steps {
				sh 'ls -la'
				sh 'sudo chmod -R 755 \$PWD/'
				sh 'cat /var/jenkins_home/workspace/jenkin-devops-microservice-pipeline@tmp/durable-6871a562/script.sh'	  
				
			}
		}

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