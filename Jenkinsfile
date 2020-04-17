pipeline {

    agent none

    stages {

        stage("Fix the permission issue") {

            agent any

            steps {
                sh "sudo chown root:jenkins /run/docker.sock"
            }

        }

        stage('Step 1') {

            agent {
                docker {
                    image 'nezarfadle/tools'
                    reuseNode true
                }
            }

            steps {
                sh "ls /"
            }

        }

    }
}
