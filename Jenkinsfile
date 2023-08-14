pipeline {
	agent any
	   stages {
	        stage('Clone Repository') {
	        steps {
	        checkout scm
	        }
	   }
	   stage('Build Image') {
	        steps {
	        bat 'docker build -t nlp-mlops:v1 .'
	        }
	   }
	   stage('Run Image') {
	        steps {
	        bat 'docker run -p 5000:8000 -d --name mynlp nlp-mlops:v1'
	        }
	   }
	   stage('Testing'){
	        steps {
	            echo 'Testing..'
	            }
	   }
    }
}