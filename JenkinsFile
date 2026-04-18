pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/sxtest93/checkovTest.git'
            }
        }

        stage('Install Checkov') {
            steps {
                sh '''
                pip3 install --upgrade checkov
                '''
            }
        }

        stage('Run Checkov Scan') {
            steps {
                sh '''
                checkov -d . --output cli
                '''
            }
        }
    }
}
