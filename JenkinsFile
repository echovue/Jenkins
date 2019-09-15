#!/usr/bin/env groovy

pipeline {
    agent { label 'executor' }
    
    stages {
        stage('Build container image') {
            steps {
                sh './build.sh'
            }
        }
        
        stage('Test container') {
            steps {
                sh './test.sh'
            }
        }
        
        stage('Push container to DockerHub') {
            steps {
                sh './push.sh'
            }
        }
    }
}
