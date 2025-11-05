pipeline {
    agent any

    stages {
        stage ('one') {
            steps {
                sh "rm -rf /root/.jenkins/workspace/test/master/index.html"
            }
        }
        stage ('two') {
            steps {
                sh "docker run -dp 8080:80 --name s3 httpd"
            }
        }
        stage ('three') {
            steps {
                sh "git clone https://github.com/SaurabhWazade/vel-app.git"
            }
        }
        stage ('four') {
            steps {
                sh "docker cp /root/.jenkins/workspace/test2/master/index.html s3:/usr/local/apache2/htdocs/"
            }
        }   
    }
}
