pipeline {
    agent any
    stages {
      
        stage('Build') {
            steps {
                    // Compile the .cpp file using a shell script
                    build 'PES2UG21CS590-1'
                    sh 'g++ main.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                    // Execute the compiled .cpp file and print its output
                    sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                // Add deployment steps here if needed
                  echo 'deploy'
            }
        }
    }
    
    post {
        failure {
          error 'Pipeline Failed'
        }
    }
}
