pipeline {
    agent any

    stages {
    
        stage ('one') {
            steps {
                sh "docker exec s1 sh -c "chmod 777 /usr/local/apache2/htdocs/index.html"
            }
        }   
    }
}
