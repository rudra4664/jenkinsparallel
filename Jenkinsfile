pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                echo 'This is build'
            }
        }
        stage('Test Paralelly') {
            parallel {
                stage('Test on Chrome') {
                    agent any
                    steps {
                        echo 'This is test on chrome browser'
                    }
                }
                stage('Test on Safari') {
                    agent any
                    steps {
                        echo 'This is test on Safari browser'
                    }
                }
            }
            steps {
                echo 'This is test'
            }
        }
        stage('Deploy') {
            agent any
            steps {
                echo 'This is deploy'
            }
        }
    }
}
