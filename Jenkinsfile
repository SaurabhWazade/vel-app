pipeline {
    agent any

    stages {
        stage ('one') {
            steps {
                sh "docker run -dp 8090:80 --name s4 httpd"
            }
        }
        stage ('two') {
            steps {
                sh "git clone https://github.com/SaurabhWazade/vel-app.git"
            }
        }
       stage ('four') {
            steps {
                sh '''docker cp /root/.jenkins/workspace/test2/index.html s4:/usr/local/apache2/htdocs/
                docker exec s4 sh -c "chmod 644 /usr/local/apache2/htdocs/index.html"'''
    }
}
    }
}
