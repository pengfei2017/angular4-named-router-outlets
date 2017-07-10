pipeline {
    agent { docker 'reg.hepengfei.com:5000/ubuntu-angular-cli' }
    stages {
        stage('build') {
            steps {
                echo 'build'
                sh 'node --version'
                sh 'npm --version'
            }
        }
        stage('Deploy - Staging') {
            steps {
                echo 'staging'
                echo 'run-smoke-tests'
            }
        }
        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }
        stage('Deploy - Production') {
            steps {
                echo 'production'
            }
        }
    }
}
