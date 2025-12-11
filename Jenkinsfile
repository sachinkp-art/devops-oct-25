pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/sachinkp-art/devops-oct-25.git'
            }
        }

        stage('Parallel Build & Test') {
            parallel {
                stage('Build') {
                    steps {
                        echo "Building the application..."
                        sh "sleep 5"   
                    }
                }

                stage('Run Tests') {
                    steps {
                        echo "Running test cases..."
                        sh "sleep 5"   
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application..."
                echo "this is to check github webhook"
            }
        }

    }
}
