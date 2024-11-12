pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/emansajjad/jenkins-website-ci-assignment-'
            }
        }
        
        stage('Build Website') {
            steps {
                bat 'hello.bat'
            }
        }
        
        stage('HTML Validation') {
            steps {
                echo 'Running HTML Validation...'
                bat 'tidy -q -e index.html || echo "HTML issues detected!"'
            }
        }
    }
}
