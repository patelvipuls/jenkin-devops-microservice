pipeline {

    agent none

    stages {

		stage("permission") {

			agent any

			steps {
			
				sh 'usermod -aG docker jenkins'
				sh 'chmod -R 755 \$PWD/'
				sh 'whoami'
				sh 'pwd'
				echo 'listing files:'
				sh 'ls -lt'
			//	sh 'cat \$PWD@tmp/durable-6871a562/script.sh'	  
				
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