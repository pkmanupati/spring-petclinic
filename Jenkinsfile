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
				sh 'cat /etc/os-release'
			}
		}
	}
}
