pipeline {
    agent any

    stages {
        stage('Lint') {
            steps {
                echo "Running code linting..."
                // Assuming your Makefile has a 'lint' target
                sh 'make lint'
                echo "Linting Passed!"
            }
        }
        
        stage('Test') {
            steps {
                echo "Running tests..."
                // Assuming your Makefile has a 'test' target
                sh 'make test'
                echo "Tests Passed!"
            }
        }
    }
}
