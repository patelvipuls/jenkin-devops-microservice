pipeline {

    agent none

    stages {

		stage("permission") {

			agent any

			steps {
				sh  'echo path--> $PATH'
				sh 'chmod -R 775 \$PWD/'
				sh 'whoami'
				sh 'pwd'
				echo 'listing files:'
				sh 'ls -lt'
			//	sh 'cat \$PWD@tmp/durable-6871a562/script.sh'	  
				
			}
		}

		stage('install maven') {

			agent any

            steps {
			        sh 'docker pull maven:3.6.3'
					sh 'mvn --version'
            }

        }

	}
}