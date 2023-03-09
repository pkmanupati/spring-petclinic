#!groovy
pipeline {
	agent any
	stages {
		stage('Maven install') {
			agent {
				docker {
					image 'maven:3.5.0'
				}
			}
			steps {
				sh 'mvn clean install'
			}
		}
                
                 stage('Docker build') {
                         
                         agent any
                         
                         steps {
                                sh 'docker build -t demo/spring-petclinic:latest .'
                        }
		}
	}
}
