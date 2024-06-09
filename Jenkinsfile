pipeline {
    agent any

    stages {
        stage('Code Fetch') {
            steps {
                echo 'Code fetch from GitHub'
                git url: 'https://github.com/Pratyush649a/hbl.jenkins.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t my-new-website .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy on container'
                sh 'docker run -d -p 80:80 my-new-website'
            }
        }
    }
}