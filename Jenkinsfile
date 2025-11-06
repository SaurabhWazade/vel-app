pipeline {
    agent any

    stages {
        stage ('one') {
            steps {
                sh "docker run -dp 8080:80 --name s3 httpd"
            }
        }
        stage ('two') {
            steps {
                sh "git clone https://github.com/SaurabhWazade/vel-app.git"
            }
        }
        stage ('three') {
            steps {
                sh "docker cp /root/.jenkins/workspace/test2/index.html s3:/usr/local/apache2/htdocs/"
            }
        }   
    }
}
