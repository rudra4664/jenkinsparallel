pipeline {
    agent none
    parameters {
        parameters {
        string defaultValue: 'TEST', description: 'Environment to deploy the application', name: 'ENV', trim: true
        choice choices: ['main', 'master'], description: 'environment to deploy the application', name: 'BRNACH'
        }

        stages {
            stage('Build') {
            agent any
                    steps {
                        echo 'Deploying to $ENV'
                        echo 'code from $BRANCH branch'
                    }
            }
            stage('Test Paralelly') {
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
                agent { label 'Label1' }
                    steps {
                        echo 'This is test'
                    }
            }
            stage('Deploy') {
                agent { label 'Label2' }
                    steps {
                        echo 'This is deploy'
                    }
            }
        }
}
