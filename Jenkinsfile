#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'make project_workspace'
                sh 'make install'
            }
        }
        stage('Test') {
            steps {
                sh 'make start'
            }
        }
        stage('Deploy') {
            steps {
                sh 'make release'
                sh 'make deploy.ghpages'
            }
        }
    }
}
