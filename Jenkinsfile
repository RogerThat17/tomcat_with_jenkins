pipeline {
    agent any
    stages {
        stage('Build WAR file') {
            steps {
                maven('clean package', 'pom.xml')
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
