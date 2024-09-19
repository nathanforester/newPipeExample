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
        stage('change permissions') {
            steps {
                sh '''
                      sudo chown ubuntu /var/www/html/index.html
                   '''
            }
        }
            stage('write to file') {
            steps {
                sh '''
                      echo "<h1> Hello from server </h1>" > /var/www/html/index.html
                   '''
            }
    }
}
}
