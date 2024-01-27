pipeline {
    agent {
        node { label 'workstation' }
    }

    stages {

        stage('Unit Tests') {
            steps {
                echo 'Unit Tests'
            }
        }

        stage('Code Analysis') {
            steps {
              sh 'sudo sonar-scanner -Dsonar.host.url=http://172.31.40.52:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=frontend -Dsonar.qualitygate.wait=true'
            }
        }

        stage('Security Scans') {
            steps {
                echo 'Security Scans'
            }
        }

        stage('Publish Artifact') {
            steps {
                echo 'Publish Artifacts'
            }
        }
    }
}
