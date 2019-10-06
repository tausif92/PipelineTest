pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
                echo "initialized"
            }
        }
        stage ('Deploy') {
            steps {
                echo "deployed"
            }
            post {
                success {
                    echo "Passed..."
                }
            }
        }
    }
}