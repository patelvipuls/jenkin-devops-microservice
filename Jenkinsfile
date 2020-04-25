pipeline {
    agent any
    stages {
        stage('install node modules...') {
            agent { 
				docker 
					{ 
    					image 'node:8'
   						 args '-u root:root'
					} 
			}				
            steps {
                sh 'cd /path/to/package.json; yarn install'
            }
        }
    }
}