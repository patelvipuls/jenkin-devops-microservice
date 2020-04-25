pipeline {

    agent none

    stages {

		stage("permission") {

			agent any

			steps {
			
				sh 'chmod -R 775 \$PWD/'
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
					args '-u root:sudo -v $HOME/workspace/myproject:/myproject'
				}
			}

            steps {
			     	sh 'mvn --version'
            }

        }

	}
}