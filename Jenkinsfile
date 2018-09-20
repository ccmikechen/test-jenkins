pipeline {
    agent any
    stages {
        stage('Download') {
            steps {
                echo env.BRANCH_NAME
            }
        }
        stage('test') {
            when {
                not {
                    anyOf {
                        branch 'develop'
                        branch 'master'
                    }
                }
            }
            steps {
                echo 'test!'
                sh 'ls -al'
            }
        }
        stage('develop') {
            when {
                anyOf {
                    branch 'develop'
                    branch 'test'
                }
            }
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
