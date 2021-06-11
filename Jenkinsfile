pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...Webhook-Git Scm Polling'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}