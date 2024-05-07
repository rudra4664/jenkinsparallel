pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                echo 'This is Build stage'
            }
        }
        stage('Test Parallelly') {
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
        }
        stage('Deploy') {
            agent any
            steps {
                echo 'This is deploy'
            }
        }
    }
}
