pipeline {
    agent any
    stages {
        stage('Download') {
            steps {
                echo env.BRANCH_NAME
                git url: 'https://github.com/ccmikechen/test-jenkins', branch: env.BRANCH_NAME
            }
        }
        stage('develop') {
            when { branch 'develop' }
            steps {
                echo 'in develop!!'
                sh 'cat test'
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
