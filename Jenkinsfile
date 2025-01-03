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
        
    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
}
