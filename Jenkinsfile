pipeline {
    agent any
    
    stages {
        stage('Hello World') {
            steps {
                echo 'Hello from Jenkins Pipeline!'
                echo '========================='
                echo 'This is a demo pipeline'
                echo '========================='
            }
        }
        
        stage('Environment Info') {
            steps {
                echo 'Printing environment information:'
                sh 'echo "Current user: $(whoami)"'
                sh 'echo "Current directory: $(pwd)"'
                sh 'echo "Date and time: $(date)"'
                sh 'echo "Operating system: $(uname -a)"'
            }
        }
        
        stage('Simple Calculations') {
            steps {
                echo 'Performing some calculations:'
                sh 'echo "2 + 2 = $((2 + 2))"'
                sh 'echo "10 * 5 = $((10 * 5))"'
                sh 'echo "100 / 4 = $((100 / 4))"'
            }
        }
        
        stage('File Operations') {
            steps {
                echo 'Creating and reading a temporary file:'
                sh 'echo "Hello from a file!" > temp.txt'
                sh 'echo "File contents:"'
                sh 'cat temp.txt'
                sh 'echo "File created successfully!"'
                sh 'rm temp.txt'
                echo 'Temporary file cleaned up'
            }
        }
        
        stage('Final Message') {
            steps {
                echo '🎉 Pipeline completed successfully! 🎉'
                echo 'Check the console output above for all the printed messages'
                sh 'echo "Build finished at: $(date)"'
            }
        }
    }
    
    post {
        always {
            echo 'This message will always print, regardless of build result'
        }
        success {
            echo '✅ Build was successful!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}
