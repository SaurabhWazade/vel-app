pipeline {
    agent any

    stages {
        stage ('one') {
            steps {
                sh """yum install docker -y
                systemctl start docker"""
            }
        }
        stage ('two') {
            steps {
                sh "docker run -itd --name s1 httpd"
            }
        }
        stage ('three') {
            steps {
                sh "git clone "
            }
        }
    }
}
