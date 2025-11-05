pipeline {
    agent any

    stages {
        stage ('one') {
            steps {
                sh """rm -rf /root/.jenkins/workspace/test/master/index.html
                yum install docker -y
                systemctl start docker"""
            }
        }
        stage ('two') {
            steps {
                sh "docker run -dp 80:80 --name s1 httpd"
            }
        }
        stage ('three') {
            steps {
                sh "git clone https://github.com/SaurabhWazade/vel-app.git"
            }
        }
        stage ('four') {
            steps {
                sh "docker cp /root/.jenkins/workspace/test1/master/index.html s1:/usr/local/apache2/htdocs/"
            }
        }   
    }
}
}

