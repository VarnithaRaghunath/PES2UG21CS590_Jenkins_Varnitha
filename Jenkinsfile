pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                build 'PES2UG21CS590-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                // sh './output'
                sh 'exit 1'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
