pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git url: 'https://github.com/hamzaafzaalofficial/test.git', branch: 'main'
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    def startTime = System.currentTimeMillis()
                    echo 'Deploying...'
                    // Simulate deployment time
                    sh 'sleep 300'
                    def endTime = System.currentTimeMillis()
                    def deployTime = (endTime - startTime) / 1000
                    echo "Deploy time: ${deployTime} seconds"
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}


