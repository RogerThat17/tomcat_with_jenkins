pipeline {
    agent any
    stages {
        stage('Build WAR file') {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo "Archiving the artifacts"
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }
    }
}
