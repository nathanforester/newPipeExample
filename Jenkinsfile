pipeline {
    agent any
    parameters {
        booleanParam(name: 'Refresh',
                    defaultValue: false,
                    description: 'Read Jenkinsfile and exit.')
		    }
    
      stages {

        stage('update apt cache') {
            steps {
                sh '''
                      sudo apt update
                   '''
            }
        }
         stage('install apache') {
            steps {
                sh '''
                      sudo apt install apache2 -y
                   '''
            }
        }
        stage('create file') {
            steps {
                sh '''
                      touch /home/ubuntu/hello.txt
                   '''
            }
    }
}