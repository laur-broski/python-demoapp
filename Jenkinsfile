pipeline {
    agent any

    stages {

        stage('Python_check') {
            steps {
              sh 'python3 --version || python --version'
              sh 'python3 -m ensurepip --upgrade'
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
