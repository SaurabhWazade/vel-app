pipeline {
    agent any

    stages {
    
        stage ('one') {
            steps {
                sh 'docker exec s1 sh -c "chmod 644 /usr/local/apache2/htdocs/index.html"'
            }
        }   
    }
}
