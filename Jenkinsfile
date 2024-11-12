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
                sh './hello.sh'
            }
        }
        
        stage('HTML Validation') {
            steps {
                echo 'Running HTML Validation...'
                sh 'tidy -q -e index.html || echo "HTML issues detected!"'
            }
        }
    }
}
