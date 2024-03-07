pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o output YOUR_SRN-1.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Intentional error: Trying to execute a non-existing script
                    sh './non_existing_script.sh'
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


