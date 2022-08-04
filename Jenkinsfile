pipeline {
    agent { label 'master' }
    stages {
        stage('build') {
            agent { label 'dev' }
            steps {
                sh 'docker build -t testdev .'
            }
        }
        stage('Deploy') {
            agent { label 'prod' }
            steps {
                echo 'Deploying....'
            }
        }
    }
}