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
                sh "docker run -dp 90:80 --name s2 httpd"
            }
        }
        stage ('three') {
            steps {
                sh "git clone https://github.com/SaurabhWazade/vel-app.git"
            }
        }
        stage ('four') {
            steps {
                sh "docker cp /root/.jenkins/workspace/test1/2025Q1/index.html s2:/usr/local/apache2/htdocs/"
            }
        }   
    }
}

