pipeline {
    agent any

    stages {
    
        stage ('one') {
            steps {
                sh "docker cp /root/.jenkins/workspace/test/index.html s1:/usr/local/apache2/htdocs/"
            }
        }   
    }
}
