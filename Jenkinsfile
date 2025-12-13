pipeline {
  agent any
  stages {
	stage('Checkout') {
	  steps {
		git branch: 'main',
		  url: 'https://github.com/Ali2002Nazari/devops-ci-cd-project.git'
	  }
	}
	stage('Build Docker Image') {
	  steps {
		sh 'docker build -t devops-flask-app .'
	  }
	}
  }
}
