pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
                echo "initialized"
            }
        }
	stage ('Build jenkins job') {
            steps {
                echo "Building jenkins job"
		build job : 'Test1'
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