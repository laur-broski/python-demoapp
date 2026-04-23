pipeline {
    agent any

    stages {

        stage('Python_check') {
            steps {
              sh 'python --version'
              sh 'python -m ensurepip --upgrade'
            }    
        }

        stage('Lint') {
            steps {
                echo "Running code linting..."
                sh 'make lint'
                echo "Linting Passed!"
            }
        }
        
        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'make test'
                echo "Tests Passed!"
            }
        }
    }
}
