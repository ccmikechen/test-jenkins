pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                echo 'Hello'
                echo 'HHHHELO'
            }
        }
        stage('develop') {
            when { branch 'develop' }
            steps {
                echo 'in develop!!'
            }
        }
        stage('master') {
            when { branch 'master' }
            steps {
                echo 'in MMMASSSTER!!'
            }
        }
        stage('result') {
            steps {
                echo 'OK'
                echo 'OOOKK'
            }
        }
    }
}
