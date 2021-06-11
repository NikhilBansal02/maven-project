pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...Webhook'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}