pipeline {
    agent any
    
    environment {
        // Ensure you have these credentials configured in your Jenkins UI
        DOCKER_CREDENTIALS_ID = 'docker-hub-credentials'
        IMAGE_NAME = 'yourdockerhubusername/hello-world-spring:latest'
    }

    stages {
        stage('Compile & Test') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Docker Build & Push') {
            steps {
                script {
                    docker.withRegistry('https://index.docker.io/v1/', "${DOCKER_CREDENTIALS_ID}") {
                        def customImage = docker.build("${IMAGE_NAME}")
                        customImage.push()
                    }
                }
            }
        }
    }
##This is the stage where ai agent will be called if the build fails##
  post {
        failure {
            echo "Pipeline failed! Triggering AI DevOps Agent for root cause analysis..."
            // This is the line that calls your Python AI agent when the build crashes
            sh 'python3 ai_agent.py current_build_log.txt'
        }
    }
}
