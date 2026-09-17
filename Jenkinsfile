pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git(
                    branch: 'main',
                    url: 'https://github.com/bbhavanasree2212-code/online-exam-report.git'
                )
            }
        }

        stage('Generate Report') {
    steps {
        bat 'C:\\Users\\bbhav\\AppData\\Local\\Python\\bin\\python.exe app.py'
    }
}

        stage('Archive Report') {
            steps {
                archiveArtifacts(
                    artifacts: 'exam_report.txt',
                    fingerprint: true
                )
            }
        }
    }
}
