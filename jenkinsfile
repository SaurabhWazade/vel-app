pipeline {
    agent {
        label {
        label 'built-in'
        customWorkspace '/mnt/pipeline'
        }
    }

    stages {
        stage('stage-1') {
            steps {
                sh 'rm -rf *'
                sh 'mkdir stage-1'
            }
        }

        stage('stage-2') {
            steps {
                dir('/mnt/pipeline1') {
                    sh 'rm -rf *'
                    sh 'mkdir stage-2'
                }
            }
        }
    }
    post {
        always {
            echo "done with this job"
        }
    }
}

