pipeline {

    agent any

    stages {

        stage('install maven 3.6.3') {

			agent { docker 'maven:3.6.3'
					args '-u root:root'
					}

            steps {
			        sh 'mvn --version'
            }

        }

	}
}
