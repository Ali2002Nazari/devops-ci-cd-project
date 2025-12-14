pipeline {
  agent any
  stages {
	stage('checkout') {
	  steps {
		git branch: 'main',
		  url: 'https://github.com/Ali2002Nazari/devops-ci-cd-project.git
	  }
	}
	stage('Build Docker Image')
	  steps {
		sh 'docker build -t devops-flask-app .'
	  }
	}
	stage('Deploy') {
	  steps {
		sh '''
		docker rm -f flask-app || true
		docker run -d -p 5000:5000 --name flask-app devops-flask-app
		'''
	  }
	}
  }
}
