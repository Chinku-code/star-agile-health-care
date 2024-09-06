pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Chinku-code/star-agile-health-care.git'
            }
        }

        stage('Build') {
            steps {
                // List files in the directory
                sh 'ls -la'
                // Ensure that the script is executable
                sh 'chmod +x scripts/build.sh'
                // Execute the build script
                sh './scripts/build.sh'
            }
        }

        stage('Deploy') {
            steps {
                // Your deploy steps here
                echo 'Deploying application...'
            }
        }
    }
}
