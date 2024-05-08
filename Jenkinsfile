pipeline {
    agent any
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
                    steps {
                        echo 'This is test on chrome browser'
                    }
                }
                stage('Test on Safari') {
                    steps {
                        echo 'This is test on Safari browser'
                    }
                }
            }
        }
        stage('Deploy Parallelly') {
            parallel {
                stage('Deploy1') {
                    steps {
                        echo 'This is deploy1'
                    }
                }
                stage('Deploy2') {
                    steps {
                        echo 'This is deploy2'
                    }
                }

            }
        }
    }
}
