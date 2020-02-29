pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Git') {
            steps {
                sh 'git config --global user.email georgianalinalexandru@gmail.com'
                sh 'git config --global user.name G'
            }
        }
        stage('Install') { 
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}