pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o output PES2UG21CS427-1.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Print the output of the .cpp file using a shell script
                    sh './output'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Add deployment steps if needed
                    echo 'Deployment steps go here'
                }
            }
        }
    }

    post {
        always {
            // Display 'pipeline failed' in case of any errors
            catchError {
                echo 'Pipeline succeeded'
            }
        }
    }
}


