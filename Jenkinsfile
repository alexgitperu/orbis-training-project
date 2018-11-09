#!/usr/bin/env groovy

pipeline {
    agent any
    parameters {
    	choice(
	  name: 'DEPLOY',
	  choices: ["gh-page","aws"],
	  description: "Ambiente de despliegue")
    }
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
		if ("${DEPLOY}" == "aws") {
		    sh 'make deploy.aws'
		} else {
		    sh 'make deploy.ghpages'
                }
            }
	}
    }
}
