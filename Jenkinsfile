pipeline {
    agent any

    stages {
        stage ('one') {
            steps {
                sh "docker run -dp 90:80 --name s2 httpd"
            }
        }
        stage ('two') {
            steps {
                sh "git clone https://github.com/SaurabhWazade/vel-app.git"
            }
        }
        stage ('three') {
            steps {
                sh '''docker cp /root/.jenkins/workspace/test1/index.html s2:/usr/local/apache2/htdocs/
                docker exec s2 sh -c "chmod 644 /usr/local/apache2/htdocs/index.html"'''
            }
        }   
    }
}

