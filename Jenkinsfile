pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/harshitchaudhary616/AgileAssessment07_Project2.git'
            }
        }

        stage('Generate Report') {
            steps {
                sh 'python3 app.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
