pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
                echo "initialized"
            }
	        steps {
		git([url: 'https://github.com/tausif92/PipelineTest.git', branch: 'master'])
                robot --include TC1 test1.robot
            }
	        steps {
                robot -i TC2 test1.robot
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
		        failure {
                    echo "Failed..."
                }
            }
        }
    }
}